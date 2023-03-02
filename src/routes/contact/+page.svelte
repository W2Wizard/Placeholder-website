<script lang="ts">
	import Pagesection from "$lib/components/pagesection/pagesection.svelte";
</script>

<svelte:head>
	<title>Contact Us</title>
	<meta name="contact" content="Contact us about any inquiry." />
</svelte:head>

<Pagesection style="background-color: coral; color: white;">
	<div class="content">
		<h1>Contact</h1>
	</div>
</Pagesection>

<style lang="scss">
	div.content {
		display: flex;
		flex-direction: column;
	}
</style>
