<script>
   let members =[
        {
            name: "Aayan Agarwal",
            role: 'Prez',
            pfp: 'https://i.imgur.com/Rb6fHNy.png',
            socials: [
                'https://www.facebook.com/john.doe',
                'https://www.instagram.com/john.doe',
                'https://www.twitter.com/john.doe'
            ]
        },
        {
            name: "Aayush Garg",
            role: 'VP',
            pfp: 'https://i.imgur.com/Rb6fHNy.png',
            socials: [
                'https://www.facebook.com/john.doe',
                'https://www.instagram.com/john.doe',
                'https://www.twitter.com/john.doe'
            ]
        },
        {   
            name: "Yuvraaj Narula",
            role: 'Sec',
            pfp: 'https://i.imgur.com/Rb6fHNy.png',
            socials: [
                'https://www.facebook.com/john.doe',
                'https://www.instagram.com/john.doe',
                'https://www.twitter.com/john.doe'
            ]
        }
    ];
</script>
<style>
    .current-members{
        display: flex;
        position: absolute;
        width: 150vh;
        margin-top: 16.5vw;
        margin-left: 10vw;
        justify-content: space-between;
    }
    .current-members img{
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
    }
    .member-info h4{
        font-weight: lighter;
        color: #666;
        font-size: 1.3vw;
        margin-top: -1vw;
    }
    .card{
        width: 41.3vh;
        height:48.75vh;
        background: #191919;
        border-radius: .75vw;
        transition: all 0.5s ease;
        cursor: pointer;
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
        margin-top: 1.5vw;
        opacity: 1;
    }
    button{
        position: absolute;
        margin-top:48.5vw;
        margin-left: 35%;
        background:transparent;
        font-size: 1.5vw;
        color: #eee;
        border: none;
        cursor: pointer;
    }
    button i {
        margin-left: 1vw;
    }
</style>
<div class="member-info">
    <div class="current-members">
        {#each members as member}
            <div class="card">
                <img src="{member.pfp}" alt="{member.name}'s picture">
                <div class="member-info">
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
    <button>
        drag <i class="fa-solid fa-arrow-right-long"></i>
    </button>
</div>
