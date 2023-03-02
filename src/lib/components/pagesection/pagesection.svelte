<script lang="ts">
	export let style: string | null = null;
</script>

<section {style}>
	<div class="content">
		<slot />
	</div>
</section>

<style lang="scss">
	section {
		position: relative;
		min-height: calc(100vh - var(--header-height) * 2);
		padding: 6rem 2em 0rem 2em;
	}

	div {
		padding: 3rem 1.5rem;
	}
</style>