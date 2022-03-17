<style>
    .alumni-members{
        display: flex;
        position: absolute;
        width: 150%;
        height: 70vh;
        overflow-x: scroll;
        margin-top: 16.5vw;
        margin-left: 10vw;
        justify-content: space-between;
        cursor: grab;
        animation: slide-in-left 1s ease; 
    }
    @keyframes slide-in-left{
        from{
            opacity: 0;
            margin-left: 50vw;
        }
        to{
            opacity: 1;
            margin-left: 10vw;
        }
    }
    .alumni-members img{
        width: 32vh;
        height: 30vh;
        display: block;
        margin-left: auto;
        margin-right: auto;
        margin-top: 2.5vw;
        border-radius: 1vw;
    }
    .member-info{
        text-align: center;
    }
    .member-info h2{
        font-size: 2vw;
        font-weight: lighter;
        margin-top: -1vw;
    }
    .member-info h4{
        font-weight: lighter;
        color: #666;
        font-size: 1.3vw;
        margin-top: -1vw;
    }
    .member-info h3{
        color: #16e16e;
    }
    .card{
        width: 41.3vh;
        height:52.5vh;
        background: #191919;
        border-radius: .75vw;
        transition: all 0.5s ease;
    }
    .social-info{
        background: #393939;
        width: 55%;
        height: 3.5vh;
        border-radius: .5vw;
        margin-left: auto;
        margin-right: auto;
        margin-top: 5vw;
        transition: all 0.5s ease;
        opacity: 0;
        padding-top: 1vw;
        padding-bottom: 1vw;
    }
    .social-info a{
        color: white;
        text-decoration: none;
        font-size: 1.5vw;
        margin-left: .25vw;
        margin-right: .25vw;
    }
    .card:hover{
        height: 53.5vh;
        box-shadow: rgba(0,0,0,0.5) 0 0 10px;
    }
    .card:hover .social-info{
        margin-top: -1vw;
        opacity: 1;
    }
    button{
        position: absolute;
        margin-top:50vw;
        margin-left: 35%;
        background:transparent;
        font-size: 1.5vw;
        color: #eee;
        border: none;
    }
    button i {
        margin-left: 1vw;
    }
    form input{
        width: 8.75vh;
        transition: all 0.5s ease;
        border: none;
        background: transparent;
        padding-bottom: .25vw;
        font-size: 1.5vw;
        position: absolute;
        margin-top: 50vw;
        margin-left: -41.5vw;
        color: #eee !important;
    }
    form input:focus{
        width: 32.5vh;
        outline: none;
        border-bottom: 0.25vw solid #16e16e;
    }
    form input::placeholder{
        color: #eee;
    }
    .slider {
        position: absolute;
        width: 150vh;
        height: 65vh;
        top: 1.5%;
        left: 1.5%;
        padding-left: 1.5%;
        padding-right: 1%;
        overflow: hidden;
    }
    .slider-body{
        position: absolute;
        display: grid;
        height: 100%;
        top: 0;
        left: 0;
        grid-template-columns: repeat(15,1fr);
        gap: 3.5%;
        /* pointer-events: none; */
        transition: .5s ease-in;
    }
    .mobile-input{
        display: none;
    }
    @media only screen and (max-width: 768px){
        .search-input,button,.slider{
            display: none;
        }
        .mobile-input{
            display: block;
            margin-top: 32.5vw !important;
            margin-left: 7.5vw !important;
            position: absolute;
        }
        #mobile-search{
            width: 30vh;
            font-size: 4.5vw !important;
            background: transparent;
            border: none;
            border-bottom: 2px solid #16e16e;
            color: #eee;
            padding-left: 10px;
            padding-bottom: 5px;
        }
        #mobile-search:focus{
            outline: none;
        }
        #mobile-search::placeholder{
            color: #eee;
        }
    }
</style>
<div class="member-info">
    <div class="alumni-members">
        <div class="slider" id="slider">
            <div class="slider-body">
                {#each members as member}
                    <div class="card">
                        <img src="{member.pfp}" alt="{member.name}'s picture">
                        <div class="member-info">
                            <h3>{member.year}</h3>
                            <h2>{member.name}</h2>
                            <h4>{member.role}</h4>
                        </div>
                        <div class="social-info">
                            {#each member.socials as socials}
                                {#if socials.includes('instagram')}
                                    <a href="{socials}" target="_blank">
                                        <i class="fa-brands fa-instagram" ></i>
                                    </a>
                                {/if}
                                {#if socials.includes('facebook')}
                                    <a href="{socials}" target="_blank">
                                        <i class="fa-brands fa-facebook"></i>
                                    </a>
                                {/if}
                                {#if socials.includes('twitter')}
                                    <a href="{socials}" target="_blank">
                                        <i class="fa-brands fa-twitter"></i>
                                    </a>
                                {/if}
                            {/each}
                        </div>
                    </div>
                {/each}
            </div>
            </div>
        </div>
    <button>
        drag <i class="fa-solid fa-arrow-right-long"></i>
    </button>
    <div class="search-input">
        <form action="">
            <input id="search" class="search" type="text" placeholder="Search by name or field">
        </form>
    </div>
    <div class="mobile-input">
        <input type="text" id="mobile-search" placeholder="Search by name or field">
    </div>
</div>
<script>
    import {onMount} from 'svelte';
    import alumni from '../../data/alumni.json';
    let members = alumni
     onMount(()=>{
        let search = document.getElementById('search');
        search.addEventListener('keyup', ()=>{
            let searchValue = search.value.toLowerCase();
            let cards = document.querySelectorAll('.card');
            cards.forEach(card =>{
                let name = card.querySelector('h2').innerText.toLowerCase();
                let role = card.querySelector('h4').innerText.toLowerCase();
                let year = card.querySelector('h3').innerText 
                if(name.includes(searchValue) || role.includes(searchValue) || year.includes(searchValue)){
                    card.style.display = 'inline-block';
                }else{
                    card.style.display = 'none';
                }
            })
        })
        let draggableSlider = function () {
        let slider = document.querySelector(".slider"),
            innerSlider = document.querySelector(".slider-body");
        let pressed = false,
            startX,
            x;
    
        slider.addEventListener("mousedown", (e) => {
            pressed = true;
            startX = e.offsetX - innerSlider.offsetLeft;
            slider.style.cursor = "grabbing";
        });
    
        slider.addEventListener("mouseenter", () => {
            slider.style.cursor = "grab";
        });
    
        slider.addEventListener("mouseup", () => {
            slider.style.cursor = "grab";
        });
    
        window.addEventListener("mouseup", () => {
            pressed = false;
        });
    
        slider.addEventListener("mousemove", (e) => {
            if (!pressed) return;
            e.preventDefault();
    
            x = e.offsetX;
    
            innerSlider.style.left = `${x - startX}px`;
    
            checkBoundry();
        });
    
        // Check boundry of outer and inner sliders
        function checkBoundry() {
            let outer = slider.getBoundingClientRect(),
            inner = innerSlider.getBoundingClientRect();
    
            if (parseInt(innerSlider.style.left) > 0) {
            innerSlider.style.left = "0px";
            } else if (inner.right < outer.right) {
            innerSlider.style.left = `-${inner.width - outer.width}px`;
            }
        }
        };
        draggableSlider();
     });
 </script>