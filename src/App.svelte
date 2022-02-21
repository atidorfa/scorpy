<script>
	import Header from "./components/Header.svelte";
	import Footer from "./components/Footer.svelte";
	import Home from "./components/Home.svelte";
	import Tabs from "./components/Tabs.svelte";
	import Darkmode from "./components/Darkmode.svelte";
	
	// export let name;

	let tab_items = ['Home', 'Darkmode']
	let activeTab = 'Home'

	const tabChange = (e) => {
		activeTab = e.detail;
	}


</script>


<Header />
<main>
	<Tabs {tab_items} {activeTab} on:tabChange={tabChange} />
	{#if activeTab === 'Home'}
		<!-- HOME COMPONENT -->
		<Home />
	{:else if activeTab === 'Darkmode'}
		<!-- LOGIN COMPONENT -->
		<Darkmode />
	{/if}
</main>
<Footer />

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	/* h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	} */

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>