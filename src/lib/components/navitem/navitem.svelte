<script lang="ts">
	import { page } from "$app/stores";
	import { Icon } from "svelte-hero-icons";
	import { createEventDispatcher } from 'svelte';
	import type { IconSource } from "svelte-hero-icons";

	/** The HREF to navigate to. */
	export let href: string;
	/** The Icon to use for the button. */
	export let icon: IconSource;
	/** The Button text to display. */
	export let text: string;
</script>

<!-- HTML -->

{#if $page.route.id == href}
	<a data-sveltekit-preload-data="hover" {href}>
		<Icon src={icon} size="28px" solid style="color: var(--foreground);" />
		<p>{text}</p>
	</a>
{:else}
	<a data-sveltekit-preload-data="hover" {href}>
		<Icon src={icon} size="28px" style="color: var(--foreground);" />
		<p>{text}</p>
	</a>
{/if}

<!-- Styling -->
<style lang="scss">
	a {
		cursor: pointer;
		display: flex;

		align-items: center;
		justify-content: center;
		flex-direction: column;
		text-decoration: none;

		text-overflow: ellipsis;
		white-space: nowrap;

		padding: 4px;
		border-radius: var(--border-radius);
		text-align: center;

		color: var(--foreground);
		background: transparent;

		border: solid rgba(0, 0, 0, 0) 2px;
		transition: border-color 0.1s ease-out;
		transition-delay: 0.05s;
		outline: none;

		font-size: 16px;

		width: 64px;
		height: 64px;

		p {
			font-size: 0.8rem;
		}

		&:focus {
			border-color: var(--foreground);
		}

		&:hover {
			border-color: var(--foreground);
		}
	}
</style>
