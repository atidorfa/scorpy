<script>
    import Button from './Button.svelte'
    import { createEventDispatcher } from "svelte";
    let dispatch = createEventDispatcher();


    function buttonFunction(){
        // console.log('I was called in parent');
    }

    let data = {}

    export let value = JSON.stringify(data);

    async function doPost () {
		const res = await fetch('http://localhost:8000/scorpy/post', {
            mode: 'no-cors',
			method: 'POST',
			body: JSON.stringify({
				value
			})
        })
        .then(
            function successCallback(res){
            console.log(res);
            if (res) {  // Response will be either true or false. For this yu need to change the API response.
                openInNewTab('http://localhost:8000/scorpy/get')
                console.log('Success')
            }else{
               //Something went wrong
            }
        })
    }

    function openInNewTab(url) {
        window.open(url, '_blank').focus();
    }

</script>

<h3 class="gray_scale">
    <p>Insert your json to scorpy</p>
    <!-- <img src="/img/path" alt="mit"> -->    
</h3>

<textarea bind:value={value}></textarea>
<h3>
    <Button handleClick={() => doPost()}/>
</h3>

<style>
    /* img {
        max-width: 120px;
    }

    .gray_scale {
        filter: grayscale(100%);
        opacity: 0.6;
    } */
    
    textarea {
        width: 50%; 
        height: 200px;
        border-radius: 7px;
        padding: 20px;
    }

</style>