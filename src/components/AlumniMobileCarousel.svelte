<script>
    import { Swiper, SwiperSlide } from 'swiper/svelte';
    import 'swiper/css'
    import 'swiper/css/navigation'
    import alumni from '../../data/alumni.json';
</script>

<div class="carousel">
    <Swiper 
    spaceBetween={50}
    slidesPerView={1}
    centeredSlides={true}
    >
    {#each alumni as members}
        <SwiperSlide>
            <div class="card">
                <img src="{members.pfp}" alt="" srcset="">
                <h2>
                    {members.name}
                </h2>
                <h4>
                    {members.role}
                </h4>
                <div class="social-info">
                    {#each members.socials as socials}
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
        </SwiperSlide>
    {/each}
</Swiper>
</div>
<style>
    .carousel{
        display: none;
    }
    @media only screen and (max-width: 768px){
        .carousel{
            display: block;
            margin-left: 5vw;
            margin-top: 25vw;
        }
        .card{
            width: 41.3vh;
            height: 50vh;
            background: #191919;
            border-radius: 10px;
            text-align: center;
            transition: all 0.5s ease;
        }
        .card img{
            width: 32vh;
            height: 30vh;
            margin-top: 9.5vw;
            border-radius: 10px;
        }
        .card h2 {
            font-size: 7.5vw;
        }
        .card h4{
            color: #666;
            font-size: 5vw;
            margin-top: -2vw;
        }
        .card:hover{
            height: 57.5vh;
            box-shadow: rgba(0,0,0,0.5) 0 0 10px;
        }
        .social-info{
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
            font-size: 5vw;
            margin-left: 1.5vw;
            margin-right: 1.5vw;
        }
        .card:hover .social-info{
            opacity: 1;
        }
    }
</style>