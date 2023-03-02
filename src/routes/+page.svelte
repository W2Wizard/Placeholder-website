<script lang="ts">
	import Pagesection from "$lib/components/pagesection/pagesection.svelte";
</script>

<svelte:head>
	<title>Placeholder</title>
	<meta name="home" content="Place text here"/>
</svelte:head>

<Pagesection style="background-color: coral; color: white;">
	<div class="content">
		<h1>W2Wizard</h1>
		<h2>Software Engineering and memes</h2>
	</div>
</Pagesection>
<Pagesection style="background-color: green; color: white;">
	<div class="content">
		<h1>Codam</h1>
		<h2>A school for memes</h2>
	</div>
</Pagesection>
<Pagesection style="background-color: cornflowerblue; color: white;">
	<div class="content">
		<h1>You</h1>
		<h2>The actual meme itself</h2>
	</div>
</Pagesection>

<style lang="scss">

	div.content {
		display: flex;
		flex-direction: column;
	}
</style>
