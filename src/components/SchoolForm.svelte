<script>
  import { notyf } from "./notyf";

  let shorterText = false;
  const screenWidth = screen.width;

  if (screenWidth < 768) {
    shorterText = true;
  }

  window.addEventListener("resize", () => {
    const screenWidth = screen.width;
    if (screenWidth < 768) {
      shorterText = true;
    } else {
      shorterText = false;
    }
  });

  let maxParticipants = {
    Hackathon: 3,
    Designathon: 3,
    Hardware: 2,
    Crossword: 2,
    Surprise: 2,
    "Group Discussion": 1,
    Robotics: 2,
    "Paint 3D": 1,
    "Adobe Spark": 1,
    Minecraft: 2,
  };

  let checkedEvents = [];
  let schoolFields = [
    "school-name",
    "club-name",
    "club-email",
    "teacher-incharge-name",
    "teacher-incharge-number",
    "student-incharge-name",
    "student-incharge-number",
  ];
  let participantFields = ["Name", "Class", "Email"];
  let apiProps = {
    "school-name": "schoolName",
    "club-name": "clubName",
    "club-email": "clubEmail",
    "teacher-incharge-name": "teacherIncharge",
    "teacher-incharge-number": "teacherInchargeNumber",
    "student-incharge-name": "studentIncharge",
    "student-incharge-number": "studentInchargeNumber",
  };
  const addEvent = (event) => {
    checkedEvents = [...checkedEvents, event];
  };

  const removeEvent = (event) => {
    let index = checkedEvents.indexOf(event);
    if (index !== -1) {
      checkedEvents.splice(index, 1);
    }
    checkedEvents = checkedEvents;
  };

  const submitSchoolForm = async (formData) => {
    try {
      const response = await (
        await fetch("https://ts-reg-21.herokuapp.com/school", {
          method: "POST",
          body: JSON.stringify(formData),
          headers: { "Content-Type": "application/json; charset=utf-8" },
        })
      ).json();
      return { success: true, message: response };
    } catch (err) {
      return { success: false, message: err };
    }
  };

  window.addEventListener("click", (e) => {
    if (e.target.checked === false) {
      if (checkedEvents.includes(e.target.value)) {
        removeEvent(e.target.value);
      }
    } else if (e.target.checked === true) {
      addEvent(e.target.value);
    }
  });

  const handleSubmit = async () => {
    let formData = {};
    formData["events"] = checkedEvents;
    let errors = [];
    schoolFields.forEach((f) => {
      if (document.getElementsByClassName(f)[0].value.trim().length !== 0) {
        formData[apiProps[f]] = document.getElementsByClassName(f)[0].value;
      } else {
        let eventFullName = "";
        f.split("-").forEach((e) => {
          eventFullName += `${e[0].toUpperCase()}${e.slice(1, e.length)} `;
        });
        errors.push(`Please fill in ${eventFullName.toLowerCase().trim()}.`);
      }
    });

    const recaptchaResponse = grecaptcha.getResponse();
    if (recaptchaResponse.length === 0) {
      notyf.error("CAPTCHA verification failed. Please try again.");
      return;
    }

    notyf.success({
      message: "Submitting your form.",
      duration: 0,
      dismissible: false,
    });

    if (errors.length === 0) {
      checkedEvents.forEach((ce) => {
        for (let i = 1; i < maxParticipants[ce] + 1; i++) {
          let eventname = "";
          eventname = ce.toLowerCase().split(" ").join("");
          let fieldName = `${eventname}P${i}`;
          let participant = {};
          participantFields.forEach((pf) => {
            let eventClassName = ce + "-" + i + "-" + pf;
            let detailName = "";
            if (pf === "Class") {
              detailName = "cls";
            } else {
              detailName = pf.toLowerCase();
            }
            if (document.getElementsByClassName(eventClassName)[0].value.trim().length !== 0) {
              participant[detailName] = document.getElementsByClassName(eventClassName)[0].value;
            } else {
              participant[detailName] = "undefined";
            }
          });
          formData[fieldName] = participant;
        }
      });
    } else {
      notyf.dismissAll();
      errors.forEach((err) => notyf.error(err));
      return;
    }

    const status = await submitSchoolForm(formData);

    if (status.success) {
      notyf.dismissAll();
      notyf.success(status.message);
      setTimeout(() => window.location.reload(), 2000);
      return;
    } else {
      notyf.error(status.message);
      notyf.dismissAll();
      return;
    }
  };
</script>

<svelte:head>
  <script src="https://www.google.com/recaptcha/api.js" async defer></script>
</svelte:head>

<p>School Name</p>
<input
  type="text"
  placeholder="Amity International School, Sector-46"
  class="school-name"
/>
<div class="inline">
  <div>
    <p>Club Name</p>
    <input
      type="text"
      placeholder="Tech Syndicate"
      id="inline-input"
      class="club-name"
    />
  </div>
  <div>
    <p>Club Email</p>
    <input
      type="text"
      placeholder="ts@gmail.com"
      id="longer-inline-input"
      class="club-email"
    />
  </div>
</div>
<div class="inline">
  <div>
    <p>Teacher Incharge</p>
    <input
      type="text"
      placeholder="Chanchal Dhingra"
      id="inline-input"
      class="teacher-incharge-name"
    />
  </div>
  <div>
    <p>Teacher Incharge Number</p>
    <input
      type="text"
      placeholder="+91 9090909090"
      id="longer-inline-input"
      class="teacher-incharge-number"
    />
  </div>
</div>
<div class="inline">
  <div>
    <p>Student Incharge</p>
    <input
      type="text"
      placeholder="Anshul Saha"
      id="inline-input"
      class="student-incharge-name"
    />
  </div>
  <div>
    <p>Student Incharge Number</p>
    <input
      type="text"
      placeholder="+91 8080808080"
      id="longer-inline-input"
      class="student-incharge-number"
    />
  </div>
</div>
<p>Choose Events</p>
<div class="checkboxes">
  <div class="left">
    <label for="checkid" style="word-wrap: break-word"
      ><input
        id="checkbox-id"
        name="checkid"
        type="checkbox"
        value="Hackathon"
        class="larger"
      /><span class="text">Hackathon</span></label
    ><br />
    <label for="checkid" style="word-wrap: break-word"
      ><input
        id="checkbox-id"
        name="checkid"
        type="checkbox"
        value="Designathon"
        class="larger"
      /><span class="text">Designathon</span></label
    ><br />
    <label for="checkid" style="word-wrap: break-word"
      ><input
        id="checkbox-id"
        name="checkid"
        type="checkbox"
        value="Crossword"
        class="larger"
      /><span class="text">Crossword</span></label
    ><br />
  </div>
  <div class="left side">
    <label for="checkid" style="word-wrap: break-word"
      ><input
        id="checkbox-id"
        name="checkid"
        type="checkbox"
        value="Group Discussion"
        class="larger"
      /><span class="text">Group Discussion</span></label
    ><br />
    <label for="checkid" style="word-wrap: break-word"
      ><input
        id="checkbox-id"
        name="checkid"
        type="checkbox"
        value="Surprise"
        class="larger"
      /><span class="text">Surprise</span></label
    ><br />
    <label for="checkid" style="word-wrap: break-word"
      ><input
        id="checkbox-id"
        name="checkid"
        type="checkbox"
        value="Hardware"
        class="larger"
      /><span class="text">Hardware</span></label
    ><br />
  </div>
  <div class="left side">
    <label for="checkid" style="word-wrap: break-word"
      ><input
        id="checkbox-id"
        name="checkid"
        type="checkbox"
        value="Robotics"
        class="larger"
      /><span class="text">Robotics</span></label
    ><br />
    <label for="checkid" style="word-wrap: break-word"
      ><input
        id="checkbox-id"
        name="checkid"
        type="checkbox"
        value="Minecraft"
        class="larger"
      /><span class="text">Minecraft</span></label
    ><br />
    <label for="checkid" style="word-wrap: break-word"
      ><input
        id="checkbox-id"
        name="checkid"
        type="checkbox"
        value="Adobe Spark"
        class="larger"
      /><span class="text">Adobe Spark</span></label
    ><br />
  </div>
  <div class="right">
    <label for="checkid" style="word-wrap: break-word"
      ><input
        id="checkbox-id"
        name="checkid"
        type="checkbox"
        value="Paint 3D"
        class="larger"
      /><span class="text">Paint 3D</span></label
    ><br />
  </div>
</div>

{#each checkedEvents as event}
  <p id="event-name">{event}</p>
  {#each [...Array(maxParticipants[event]).keys()] as index}
    <div class="inline">
      <div>
        <p>
          {shorterText ? `P${index + 1} Name` : `Participant ${index + 1} Name`}
        </p>
        <input
          type="text"
          placeholder="Jane Doe"
          id="participant-name-input"
          class={event + "-" + (index + 1) + "-Name"}
        />
      </div>
      <div style="margin-left: -1vw">
        <p>
          {shorterText
            ? `P${index + 1} Class`
            : `Participant ${index + 1} Class`}
        </p>
        <input
          type="text"
          placeholder="XII"
          id="participant-class-input"
          class={event + "-" + (index + 1) + "-Class"}
        />
      </div>
      <div style="margin-left: -1vw">
        <p>
          {shorterText
            ? `P${index + 1} Email`
            : `Participant ${index + 1} Email`}
        </p>
        <input
          type="text"
          placeholder="jane@gmail.com"
          id="participant-email-input"
          class={event + "-" + (index + 1) + "-Email"}
        />
      </div>
    </div>
  {/each}
{/each}

<form id="schoolForm" on:submit|preventDefault={handleSubmit}>
  <div
    class="g-recaptcha"
    data-sitekey="6LeNPbwZAAAAAHdxxchL8tm-6X6Dx0P54tavUBfv"
    data-theme="dark"
    style="margin-top: 3vh;"
    id="recap"
  />
  <button type="submit">Register</button>
</form>

<style>
  p {
    font-size: 1vw;
    color: #16e16e;
  }

  .inline {
    display: flex;
    flex-flow: row wrap;
    align-items: center;
  }

  #inline-input {
    margin-right: 2vw;
    width: 16.5vw;
  }

  #longer-inline-input {
    width: 19.3vw;
  }

  #participant-name-input {
    margin-right: 2vw;
    width: 12.5vw;
  }

  #participant-class-input {
    margin-right: 2vw;
    width: 9vw;
  }

  #participant-email-input {
    margin-right: 2vw;
    width: 12.9vw;
  }

  input[type="text"] {
    background-color: transparent;
    height: 2.2vw;
    border: 0.01vw white solid;
    font-size: 1.2vw;
    padding-left: 1vw;
    color: white;
    width: 39vw;
    border-radius: 3px;
    margin-top: -0.5rem;
    margin-bottom: 1vw;
    padding-top: 0.3rem;
    padding-bottom: 0.3rem;
  }

  .checkboxes {
    display: flex;
    flex-flow: row wrap;
    align-items: center;
    margin-left: -0.5vw;
    margin-top: -0.5%;
    margin-bottom: 1.2vw;
  }

  .checkboxes label {
    font-size: 0.9vw;
  }

  .checkboxes .text {
    margin-left: -0.3vw;
  }

  input.larger {
    transform: scale(1.4);
    border: none;
    margin: 0.8vw;
  }

  [type="checkbox"] {
    vertical-align: middle;
  }

  .side {
    margin-left: 1vw;
  }

  .checkboxes .right {
    margin-left: 1vw;
    margin-top: -5vw;
  }

  #event-name {
    font-size: 1.5vw;
    margin-bottom: 0.5vw;
    color: white;
  }

  button {
    height: 2.5vw;
    width: 8vw;
    border: none;
    text-align: center;
    padding-left: 1vw;
    padding-right: 1vw;
    color: white;
    background-color: #00af3b;
    font-size: 1.2vw;
    border-radius: 5px;
    margin-top: 3vh;
  }

  button:hover {
    cursor: pointer;
  }

  @media screen and (max-width: 768px) {
    p {
      font-size: 3vw;
    }

    input[type="text"] {
      height: 5vw;
      width: 72vw;
      padding-left: 3vw;
      font-size: 3vw;
      margin-bottom: 3vw;
      margin-top: -1vw;
    }

    #inline-input {
      margin-right: 4vw;
      width: 32vw;
    }

    #longer-inline-input {
      width: 33vw;
    }

    #recap {
      transform: scale(0.67);
      transform-origin: 0 0;
    }

    .checkboxes label {
      font-size: 3vw;
    }

    .checkboxes .text {
      margin-left: 1vw;
    }

    input.larger {
      transform: scale(1);
      border: none;
      margin: 0.8vw;
    }

    .side {
      margin-left: 1vw;
    }

    .checkboxes .right {
      margin-left: 0vw;
      margin-top: 0.5vw;
    }

    #event-name {
      font-size: 5vw;
      margin-bottom: 0.5vw;
      color: white;
    }

    #participant-name-input {
      margin-right: 4vw;
      width: 20vw;
    }

    #participant-class-input {
      margin-right: 4vw;
      width: 10vw;
    }

    #participant-email-input {
      margin-right: 0vw;
      width: 30vw;
    }

    button {
      height: 8vw;
      width: 20vw;
      border: none;
      text-align: center;
      padding-left: 1vw;
      padding-right: 1vw;
      color: white;
      background-color: #00af3b;
      font-size: 3.5vw;
      border-radius: 5px;
      margin-top: 0vh;
    }
  }
</style>
