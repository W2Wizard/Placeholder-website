<script lang="ts">
	import Pagesection from "$lib/components/pagesection/pagesection.svelte";
</script>

<svelte:head>
	<title>About Us</title>
	<meta name="about" content="Who we are and what drives us forward." />
</svelte:head>

<Pagesection style="background-color: coral; color: white;">
	<div class="content">
		<h1>About Us</h1>
	</div>
</Pagesection>

<style lang="scss">
	div.content {
		display: flex;
		flex-direction: column;
	}
</style>
