<script>
    import Fa from 'svelte-fa'
    import { faFlag } from '@fortawesome/free-solid-svg-icons'

    export let handleClick = () => {
        // console.log('I was not called in child')
    }

</script>

<button on:click={handleClick()}>
    <Fa icon={faFlag} />
</button>

<style>
    button {
        cursor: pointer;
        background-color: #f76027;
        color: white;
        border: none;
        border-radius: 4px;
        padding: 0.7rem 1rem 0.9rem 1rem;
        text-transform: uppercase;
    }
</style>