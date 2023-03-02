<script lang="ts">
	import { page } from "$app/stores";
</script>

<div>
	<h1>{$page.status} : {$page.error?.message}</h1>
	<a href="/">Go Home</a>
</div>

<style lang="scss">
</style>
