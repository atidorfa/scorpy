<script>
    import Fa from 'svelte-fa'
    import { faArrowRight } from '@fortawesome/free-solid-svg-icons'
    import Darkmode from "./Darkmode.svelte";
</script>

<header>
    <h1>
        <h2>
            <img src="/img/scorpy.png" alt="imagen logo">
            <Fa icon={faArrowRight} />
            <img src="/img/pdfpy.png" alt="imagen logo">
        </h2>
        <p>scorpy</p>   
    </h1>
    <!-- <div><Darkmode /></div> -->
</header>



<style>
    header {
        background: #f7f7f7;
        padding: 20px;
    }

    h1 {
        margin: 0;
        text-align: center; 
    }

    img {
        max-width: 80px;
        border-radius: 15px;
        margin-bottom: -20px;
    }
    /* div {
        float: right;
        align-items: flex-end;
        position: relative;
    } */

</style>