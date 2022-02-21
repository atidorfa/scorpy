<script>
    function toggle() {
        window.document.body.classList.toggle('dark-mode')
    }
    </script>
    <button on:click={toggle}>
        <slot/>
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
        :global(body.dark-mode) button {
            background-color: #0084f6;
            color: white;
        }
    </style>