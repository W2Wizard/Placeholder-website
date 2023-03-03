<!-- Scripting -->
<script lang="ts">
	export const prerender = true
	export const ssr = false

	import "../styles.scss";
	import {
		Share,
		Chat,
		QuestionMarkCircle,
		ShoppingCart,
		Icon,
		Menu,
		Login
	} from "svelte-hero-icons";
	import Logo from "$lib/assets/logo.svg";
	import Navitem from "$lib/components/navitem/navitem.svelte";

	let navitems = [
		{
			href: "/products",
			icon: ShoppingCart,
			text: "Products"
		},
		{
			href: "/blog",
			icon: Share,
			text: "Blog"
		},
		{
			href: "/about",
			icon: QuestionMarkCircle,
			text: "About"
		},
		{
			href: "/contact",
			icon: Chat,
			text: "Contact Us"
		},
		{
			href: "/login",
			icon: Login,
			text: "Login"
		}
	];

	let hamburgerToggle: HTMLInputElement;
</script>

<!-- HTML -->

<!-- Toggle the hamburger menu when the focus changes. -->
<svelte:body
	on:focus={() => {
		hamburgerToggle.checked = false;
	}}
/>

<header>
	<nav>
		<!-- Logo -->
		<a href="/">
			<img class="logo" src={Logo} alt="42-logo" />
		</a>

		<!-- Hamburger button -->
		<label for="hamburger">
			<Icon src={Menu} size="32px" solid />
		</label>
		<input bind:this={hamburgerToggle} type="checkbox" id="hamburger" />

		<!-- Navigation pages -->
		<ul class="pages">
			{#each navitems as item}
				<Navitem {...item} />
			{/each}
		</ul>
	</nav>
</header>

<main>
	<slot />
</main>

<footer>Footer</footer>

<!-- Styling -->
<style lang="scss">
	header {
		height: var(--header-height);
	}

	header nav {
		height: inherit;
		position: fixed;
		background-color: var(--background);
		display: flex;
		width: 100%;
		align-items: center;
		justify-content: space-around;
		box-shadow: 0 0 8px black;
		z-index: 1;

		#hamburger,
		label {
			display: none;
			user-select: none;
			transition: transform 0.1s cubic-bezier(0.075, 0.82, 0.165, 1);

			&:hover {
				cursor: pointer;
			}

			&:active {
				transform: scale(0.8);
			}
		}

		.pages {
			display: flex;
			flex-direction: row;
			justify-content: center;
			align-items: center;
			gap: 8px;
			padding: 10px;
		}

		.logo {
			display: flex;
			height: 64px;
			height: 64px;
			transition: filter 0.1s ease-out;
			--glow-strength: 8px;

			&:hover {
				cursor: pointer;
				filter: drop-shadow(var(--purple) 0px 0px var(--glow-strength));
			}

			@media (prefers-color-scheme: dark) {
				filter: invert(1);
				&:hover {
					filter: invert(1) drop-shadow(var(--purple) 0px 0px var(--glow-strength));
				}
			}
		}

		// Small screens
		@media screen and (max-width: 768px) {
			.pages {
				display: none;
			}

			input:checked ~ .pages {
				display: flex;
				flex-wrap: wrap;
				background: inherit;
				// To negate the parent's flex
				position: absolute;
				// Push the entire element down by the height of the parent
				top: 100%;
				width: 100%;
				border-radius: 0 0 20px 20px;
				opacity: 1;
			}

			label {
				display: inline-block;
			}
		}
	}

	footer {
		padding: 4rem 1.5rem;
		background-color: var(--background);
	}
</style>
