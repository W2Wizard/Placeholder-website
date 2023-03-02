<script lang="ts">
	import Pagesection from "$lib/components/pagesection/pagesection.svelte";
</script>

<svelte:head>
	<title>Login</title>
	<meta name="login" content="Login into the required service." />
</svelte:head>

<Pagesection style="background-color: coral; color: white;">
	<div class="content">
		<h1>Login</h1>
	</div>
</Pagesection>

<style lang="scss">
	div.content {
		display: flex;
		flex-direction: column;
	}
</style>
