<script>
    import members from '../../data/members.json';
</script>
<div class="member-table">
    {#each members as member}
        <div class="member">
            <div class="member-pfp" style="background: url('{member.pfp}');         background-size: cover;
            background-position:center;"></div>
            <div class="member-info">
                <p class="member-name">{member.name}</p>
                <p class="member-role">{member.role}</p>
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
        color: #272727;
        transition: color 0.2s ease-in-out;
        cursor: pointer;
    }
    .member-info .socials a:hover{
        color: #16e16e;
        transform: translateY(-2px);
    }
</style>