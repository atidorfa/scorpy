<script>
    import Button from './Button.svelte'
    import { createEventDispatcher } from "svelte";
    let dispatch = createEventDispatcher();

    function buttonFunction(){
        // console.log('I was called in parent');
        alert(value)
    }

    export let value = `data = { 
    "title": {
                0: {
                    "content": "asprin",
                    "position": [0.0, 0.0],
                    "font": ["helvetica", 'B', 16],
                    "color": [220, 50, 50],
                    "cell": [210.0, 40.0, 'C', 0]
                }
    },
    "image": {
                0: {
                    "file":"static/fpdf2.png",
                    "position": [40.0, 30.0],
                    "size": [60, 60]
                },
                1: {
                    "file":"static/just_social.png",
                    "position": [100.0, 30.0],
                    "size": [60, 60]
                }
    },
    "text": {
                0: {
                    "content": f"Google Noticias es un agregador y buscador de noticias automatizado {r.json()}",
                    "position": [20.0, 100.0],
                    "font": ["helvetica", 'B', 10],
                    "color": [50, 50, 220],
                    "multi_cell": [0.0, 5.0]
                },
                1: {
                    "content": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor 
                                    incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation 
                                    ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit 
                                    in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat 
                                    non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
                    "position": [20.0, 180.0],
                    "font": ["helvetica", 'B', 16],
                    "color": [20, 150, 50],
                    "multi_cell": [80.0, 5.0]
                },
                2: {
                    "content": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor 
                                    incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation 
                                    ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit 
                                    in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat 
                                    non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
                    "position": [110.0, 180.0],
                    "font": ["helvetica", 'B', 16],
                    "color": [20, 150, 150],
                    "multi_cell": [80.0, 5.0]
                }
    }
}`;
</script>

<h3 class="gray_scale">
    <p>Insert your json to scopy</p>
    <!-- <img src="/img/path" alt="mit"> -->
    
</h3>


<!-- {@html marked(value)} -->
<textarea bind:value={value}></textarea>
<h3>
    <Button handleClick={() => buttonFunction()}/>
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