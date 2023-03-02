<script lang="ts">
	import Pagesection from "$lib/components/pagesection/pagesection.svelte";
</script>

<svelte:head>
	<title>Blog</title>
	<meta name="blog" content="Updates regarding our latest technologies." />
</svelte:head>

<Pagesection style="background-color: coral; color: white;">
	<div class="content">
		<h1>Blog</h1>
	</div>
</Pagesection>

<style lang="scss">
	div.content {
		display: flex;
		flex-direction: column;
	}
</style>
