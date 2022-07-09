<script>
    import members from '../../data/members.json';
    import {onMount} from 'svelte';
    onMount(()=>{
        let search = document.getElementById('search');
        search.addEventListener('keyup', ()=>{
            let searchValue = search.value.toLowerCase();
            let members = document.querySelectorAll('.member');
            members.forEach(member =>{
                let name = member.querySelector('.member-name').innerText.toLowerCase();
                let role = member.querySelector('.member-role').innerText.toLowerCase();
                if(name.includes(searchValue) || role.includes(searchValue)){
                    member.style.display = 'flex';
                }else{
                    member.style.display = 'none';
                }
            })
        })
    })
</script>
<div class="member-table">
    <div class="team-search">
        <svg width="45" height="45" viewBox="0 0 45 45" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M19.6875 30.9375C21.1648 30.9375 22.6277 30.6465 23.9927 30.0812C25.3576 29.5158 26.5978 28.6871 27.6424 27.6425C28.6871 26.5978 29.5157 25.3576 30.0811 23.9927C30.6465 22.6278 30.9375 21.1649 30.9375 19.6875C30.9375 18.2102 30.6465 16.7473 30.0811 15.3823C29.5157 14.0174 28.6871 12.7772 27.6424 11.7326C26.5978 10.6879 25.3576 9.85925 23.9927 9.29388C22.6277 8.72852 21.1648 8.43753 19.6875 8.43753C16.7038 8.43753 13.8423 9.62279 11.7325 11.7326C9.62273 13.8424 8.43747 16.7038 8.43747 19.6875C8.43747 22.6712 9.62273 25.5327 11.7325 27.6425C13.8423 29.7523 16.7038 30.9375 19.6875 30.9375V30.9375ZM31.5375 28.8863L38.25 35.5988C38.4289 35.7719 38.5716 35.9789 38.6697 36.2077C38.7678 36.4365 38.8194 36.6826 38.8214 36.9316C38.8233 37.1805 38.7757 37.4274 38.6813 37.6577C38.5868 37.8881 38.4475 38.0973 38.2713 38.2733C38.0951 38.4492 37.8857 38.5883 37.6552 38.6824C37.4247 38.7765 37.1778 38.8238 36.9288 38.8214C36.6798 38.8191 36.4339 38.7672 36.2052 38.6688C35.9765 38.5703 35.7697 38.4274 35.5968 38.2482L28.8843 31.5357C25.8702 33.8754 22.0777 34.9785 18.2789 34.6204C14.4801 34.2623 10.9605 32.47 8.43663 29.6083C5.91277 26.7465 4.57438 23.0306 4.69389 19.2168C4.8134 15.403 6.38185 11.7781 9.07993 9.07999C11.778 6.38191 15.4029 4.81347 19.2167 4.69395C23.0305 4.57444 26.7465 5.91283 29.6082 8.43669C32.4699 10.9605 34.2623 14.4801 34.6203 18.2789C34.9784 22.0778 33.8753 25.8703 31.5356 28.8844L31.5375 28.8863Z" fill="#747474"/>
        </svg>              
        <input type="text"  placeholder="Search" id="search">
    </div><br class="br">
    {#each members as member}
        <div class="member">
            <div class="member-pfp" style="background: url('{member.pfp}');background-size: cover;
            background-position:center;"></div>
            <div class="member-info">
                <p class="member-name">{member.name}</p>
                <p class="member-role" style="padding-bottom: 12px;">{member.role}</p>
                <div class="socials">
                    {#each member.socials as social}
                        {#if social.includes('instagram')}
                            <a href="{social}" target="_blank">
                                <i class="fa-brands fa-instagram"></i>
                            </a>
                        {/if}
                        {#if social.includes('facebook')}
                            <a href="{social}" target="_blank">
                                <i class="fa-brands fa-facebook"></i>
                            </a>
                        {/if}
                        {#if social.includes('twitter')}
                            <a href="{social}" target="_blank">
                                <i class="fa-brands fa-twitter"></i>
                            </a>
                        {/if}
                        {#if social.includes('mailto:')}
                            <a href="{social}" target="_blank">
                                <i class="fa-solid fa-envelope"></i>
                            </a>
                        {/if}
                        {#if social.includes('linkedin')}
                            <a href="{social}" target="_blank">
                                <i class="fa-brands fa-linkedin"></i>
                            </a>
                        {/if}
                        {#if social.includes('youtube')}
                            <a href="{social}" target="_blank">
                                <i class="fa-brands fa-youtube"></i>
                            </a>
                        {/if}
                        {#if social.includes('dribbble')}
                            <a href="{social}" target="_blank">
                                <i class="fa-brands fa-dribbble"></i>
                            </a>
                        {/if}
                        {#if social.includes('github')}
                            <a href="{social}" target="_blank">
                                <i class="fa-brands fa-github"></i>
                            </a>
                        {/if}
                        {#if social.includes('behance')}
                            <a href="{social}" target="_blank">
                                <i class="fa-brands fa-behance"></i>
                            </a>
                        {/if}
                        {#if social.includes('spotify')}
                            <a href="{social}" target="_blank">
                                <i class="fa-brands fa-spotify"></i>
                            </a>
                        {/if}
                        {#if social.includes('anirudhchaturvedi.me') || social.includes('aayushgarg.net')}
                            <a href="{social}" target="_blank">
                                <i class="fa-solid fa-globe"></i>
                            </a>
                        {/if}
                        {#if social.includes('soundcloud') }
                            <a href="{social}" target="_blank">
                                <i class="fa-brands fa-soundcloud"></i>
                            </a>
                        {/if}
                    {/each}
                </div>
            </div>
        </div>
    {/each}
</div>
<style>
    .member-table{
        display: grid;
        grid-template-columns: repeat(3,30vw);
        margin: 5vw 5vw;
    }
    .member{
        width: 27.5vw;
        height: 15vw;
        background: #171717;
        border-radius: 7.5px;
        margin-bottom: 2.5vw;
        display: flex;
    }
    .member .member-pfp{
        width: 10vw;
        height: 10vw;
        border-radius: 100%;
        margin: 2.5vw 2vw;
    }
    .member-info{
        margin-top: 1.75vw;
    }
    .member-info .member-name{
        font-weight: light;
        font-size: 1.75vw;
        width: 5vw;
        letter-spacing: 1px;
    }
    .member-info .member-role{
        color: #16e16e;
        margin-top: -1.25vw;
        letter-spacing: 1px;
    }
    .member-info .socials{
        margin-top:-0.5vw;
    }
    .member-info .socials i{
        margin-right: 0.5vw;
    }
    .member-info .socials a{
        text-decoration: none;
        color: #646464;
        transition: color 0.2s ease-in-out;
        cursor: pointer;
    }
    .member-info .socials a:hover{
        color: #16e16e;
        transform: translateY(-2px);
    }
    .team-search{
        display: flex;
        margin-left: 65%;
        margin-top: -7.5vw;
        position: absolute;
    }
    .team-search input{
        background:transparent;
        color: grey;
        border:none;
        border-bottom: 2px solid grey;
        border-radius: 0;
        outline: none;
        height: 2.5vw;
        width: 19.5vw;
        font-size: 1.25vw;
        padding-bottom: 0.25vw;
        transition: all .5s ease;
    }
    .team-search input:focus{
        border-bottom: 2px solid #16e16e;
        color: white;
    }
    .team-search svg{
        transform: scale(.5) translateX(40vw);
    }

    @media only screen and (max-width: 768px){
        .member-table{
            display: block;
            margin-top: 16vw;
        }
        .member{
            width: 100%;
            height: 35vw;
            margin-top: 5vw !important;
            margin-bottom: 5vw !important;
        }
        .member-info .socials i{
        margin-right: 1.5vw;
    }
        .member-info .socials a{
            font-size: 20px;
        }
        .member-info .socials{
            margin: -5vw 0.5vw;
        }
        .member .member-pfp{
            width: 20vw;
            height: 20vw;
            border-radius: 100%;
            margin: 7.5vw 5vw;
        }
        .member-info .member-name{
            font-weight: light;
            font-size: 5vw !important;
            width: auto !important;
            letter-spacing: 1px;
        }
        .member-info .member-role{
            margin-top: -2.4vw !important;
        }
        .team-search{
            display: flex;
            margin-left: 10vw !important;
            margin-top: -11vw !important;
            position: absolute;
        }
        .team-search input{
            height: 6.5vw;
            width: 42.5vw;
            font-size: 4vw;
            border-bottom: 3.5px solid grey;
            padding-bottom: 1.5vw;
        }
        .team-search input:focus{
            border-bottom: 3.5px solid #16e16e;
        }
        .team-search svg{
            transform: scale(.5) translateX(95vw) translateY(-5vw);
        }
    }
    @media screen and (min-width: 750px) and (max-width: 4000px) {
    .br {
        display:none;
    }
    }
</style>