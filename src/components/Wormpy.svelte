<script>
    import Button from './Button.svelte'
    import { createEventDispatcher } from "svelte";
    let dispatch = createEventDispatcher();


    function buttonFunction(){
        // console.log('I was called in parent');
    }


    async function doWormpy () {
        openInNewTab('https://wormpy.vercel.app/')
    }

    function openInNewTab(url) {
        window.open(url, '_blank').focus();
    }

</script>


<h3>
    <img src="/img/wormpy.png" alt="imagen logo" on:click="{() => doWormpy()}">
</h3>

<style>
    img {
        cursor: pointer;
        max-width: 80px;
    }
</style>