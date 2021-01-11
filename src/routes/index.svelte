<script>
	import jockjams from 'images/jockjams.jpg';

	let links = [
		{ href: 'https://github.com/arlenpeiffer', text: 'Github' },
		{ href: 'https://twitter.com/arlenpeiffer', text: 'Twitter' },
		{ href: 'https://bean.la', text: 'Bean.la' }
	];
</script>

<style lang="scss">
	@import "./style/main.scss";

	main {
		display: grid;
		gap: 2.5rem;
		max-width: 25rem;
		padding: 4rem 2rem;

		img {
			width: 100%;
		}

		h1 {
			font-size: $font-size;
			text-align: center;
		}

		ul {
			display: inline-grid;
			grid-auto-flow: column;
			gap: 3rem;
			place-items: center;
			margin: auto;
			@include breakpoint(mobile) {
				gap: 4rem;
			}
		}

		a {
			border-bottom: 1px solid $black;
			&:hover {
				opacity: 0.75;
			}
		}
	}
</style>

<svelte:head>
	<title>Hi. I’m Arlen. I help out with the internet.</title>
	<meta name="description" content="A personal site for the person Arlen Peiffer who does web development things" />
</svelte:head>

<main>
	<img alt="Smiley kid holding an unopened copy of Jock Jams Volume 1 on compact disc" src="{jockjams}">
	<h1>Hi. I’m Arlen. I help out with the internet.</h1>
	<ul>
		{#each links as link}
			<li>
				<a href="{link.href}" target="_blank">
					{link.text}
				</a>
			</li>
		{/each}
	</ul>
</main>
