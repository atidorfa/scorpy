<script>
	import Button from './ButtonDark.svelte'
	let name = 'scorpy';

    import Fa from 'svelte-fa'
    import { faSun } from '@fortawesome/free-solid-svg-icons'
</script>

<Button>
	<Fa icon={faSun} />
</Button>

<style>
	:global(body) {
		background-color: #f2eee2;
		color: #232323;
		transition: background-color 0.3s
	}
	:global(body.dark-mode) {
		background-color: #1d3040;
		color: #bfc2c7;
	}
</style>