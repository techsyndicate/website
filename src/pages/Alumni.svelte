<svelte:head>
  <title>TS | Alumni</title>
</svelte:head>

<script>
  import Jumbotron from "../components/Jumbotron.svelte";
  import MemberCard from "../components/MemberCard.svelte";
  import SearchBar from "../components/SearchBar.svelte";
  import alumni from "../../data/alumni.json";

  let alumniToInflate = alumni;

  const handleMessage = (event) => {
    if(event.detail.text === false) {
      alumniToInflate = alumni;
      alumniToInflate = alumniToInflate;
    } else {
      alumniToInflate = updateAlumni(event.detail.text)
    }
  }

  const updateAlumni = (q) => {
    try {
      const updatedAlumni = [
        {
          "batch": "2020-21",
          "alumni": [[]]
        },
        {
          "batch": "2019-20",
          "alumni": [[]]
        },
        {
          "batch": "2018-19",
          "alumni": [[]]
        },
        {
          "batch": "2017-18",
          "alumni": [[]]
        },
        {
          "batch": "2016-17",
          "alumni": [[]]
        },
      ]
      const alumniMatches = []
      alumni.forEach(batchObject => {
        batchObject.alumni.forEach(rows => {
          rows.forEach(a => {
            const includesName = a.name.trim().toLowerCase().includes(q.trim().toLowerCase())
            if(includesName) {
              alumniMatches.push(a)
            }
          })
        })
      })
      alumniMatches.forEach(a => {
        updatedAlumni.forEach(bo => {
          if(bo.batch === a.batch) {
            bo.alumni[0].push(a)
          }
        })
      })
      return updatedAlumni
    } catch (error) {
      return false
    }
  }

</script>

<body>
  <Jumbotron
    title="Alumni"
    description="Tech Syndicate has a vast and diverse alumni network mapped all over the globe that has been a mentor for the club's members and shaped it into what it is today."
  />
  <div style="height: 3vh" />
  <SearchBar on:message={handleMessage} />
  <div style="height: 4vh" />

  {#each alumniToInflate as batch}
    {#if batch.alumni[0].length !== 0}
      <h2>{batch.batch}</h2>
      {#each batch.alumni as row}
        <div class="container">
          {#each row as alum}
            <MemberCard
              member={alum.name}
              role={alum.exrole}
              image={alum.image}
            />
          {/each}
        </div>
        <div class="sized-box" />
      {/each}
      <div class="batch-sized-box" />
    {/if}
  {/each}
  <div style="height: 10vh;"/>
</body>

<style>
  body {
    padding: 0 18%;
  }

  .container {
    display: flex;
    justify-content: left;
  }

  .sized-box {
    height: 4vh;
  }

  @media screen and (max-width: 768px) {
    body {
      padding: 0 8%;
    }

    h2 {
      font-size: 3.6vh;
    }

    .container {
      display: block;
      justify-content: center;
    }

    .sized-box {
      height: 0;
    }

    .batch-sized-box {
      height: 2vh;
    }
  }
</style>
