<script lang="ts">
	import Pagesection from "$lib/components/pagesection/pagesection.svelte";
</script>

<svelte:head>
	<title>Products</title>
	<meta name="products" content="View our products!" />
</svelte:head>

<Pagesection style="background-color: coral; color: white;">
	<div class="content">
		<h1>Products</h1>
	</div>
</Pagesection>

<style lang="scss">
	div.content {
		display: flex;
		flex-direction: column;
	}
</style>