<script lang="ts">
	export let style: string | null = null;
</script>

<div {style} dir="ltr">
	<div class="content">
		<slot />
	</div>
</div>

<style lang="scss">
	div {
		min-height: calc(100vh - var(--header-height));
		scroll-snap-align: center;
	}

	div.content {
		padding: 6rem 2em 0rem 2em;
	}
</style>