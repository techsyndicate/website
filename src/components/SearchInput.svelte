<style>
    form input{
        width: 8.75vh;
        transition: all 0.5s ease;
        border: none;
        background: transparent;
        padding-bottom: .25vw;
        font-size: 1.5vw;
        position: absolute;
        margin-top: 48.5vw;
        margin-left: 5vw;
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
</style>
<form action="">
    <input type="text" placeholder="Search by name or field">
</form>