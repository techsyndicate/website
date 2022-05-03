<script>
    import resources from '../../data/resources.json';
</script>
<div class="learn-grid">
    {#each resources as resource}
        <div class="learn-blob">
            <div class="learn-header">
                <img src="{resource.svg}" alt="{resource.field}">
                <h2 class="learn-field">
                    {resource.field}
                </h2>
            </div>
            <p>
                {resource.info}...
            </p>
            <a href="{resource.link}" target="_blank">Know more <svg width="30" height="29" viewBox="0 0 30 29" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M2.375 16.375H23.3188L14.1688 25.525C13.4375 26.2562 13.4375 27.4562 14.1688 28.1875C14.9 28.9187 16.0813 28.9187 16.8125 28.1875L29.1688 15.8312C29.9 15.1 29.9 13.9187 29.1688 13.1875L16.8313 0.812476C16.1 0.0812256 14.9188 0.0812256 14.1875 0.812476C13.4563 1.54373 13.4563 2.72498 14.1875 3.45623L23.3188 12.625H2.375C1.34375 12.625 0.5 13.4687 0.5 14.5C0.5 15.5312 1.34375 16.375 2.375 16.375Z" fill="white"/>
                </svg>
                </a>
        </div>
    {/each}
</div>
<style>
    .learn-grid{
        display: grid;
        grid-template-columns: repeat(3, 31.25vw);
        margin: 2.5vw 5vw;
    }
    .learn-blob{
        border-radius: 7.5px;
        padding: 2vw;
        border: 2px solid #eee;
        transition: all .2s ease;
        height: 17.5vw;
        width: 25vw;
        cursor: pointer;
        margin-bottom: 2vw;
    }
    .learn-blob:hover{
        border: 2px solid #16e16e;
        transform: translateY(-5px);
    }
    .learn-header{
        display: flex;
    }
    .learn-header img{
        margin-right: 1vw;
        width: 3.5vw;
        height: 3.5vw;
        transform: translateY(1vw);
    }
    .learn-field{
        font-size: 2.5;
        letter-spacing: 1px;
    }
    .learn-blob p {
        color: #b5b5b5;
        font-size: 1.5vw;
        margin: 1vw 0.5vw;
    }
    .learn-blob a {
        color: #eee;
        text-decoration: none;
        font-size: 1.25vw;
        margin: -0.25vw 0.5vw;
    }
    .learn-blob a svg{
        transform: scale(0.5) translateX(1vw) translateY(1.25vw);
    }
</style>