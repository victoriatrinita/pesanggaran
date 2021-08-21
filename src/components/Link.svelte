<script>
	export let href;
	export let id = null;
	export let color = null;
</script>

<a
	{href}
	{id}
	on:click
	rel={href.includes('//') ? 'noopener noreferrer' : 'prefetch'}
	class:disabled={!href}
	class:orange={color !== null}
	class:deep-sea={color === 'deep-sea'}
	class:turquoise={color === 'turquoise'}
	class:tangerine-hover={color === 'tangerine-hover'}
	class:tangerine-outline={color === 'tangerine-outline'}
	class:tangerine-outline-transparent={color === 'tangerine-outline-transparent'}
	class:white={color === 'white'}
	class:none={color === null}
>
	<slot />
</a>

<style>
	a {
		flex: 0 1 7.5em;
		cursor: pointer;
		padding: 0.5em 1.25em;
		border-width: 0.15em;
		border-style: solid;
		border-radius: 3.2em;
		color: #fff;
		text-align: center;
		font-weight: 500;
		transition: 300ms;
		text-decoration: none;
	}
	a.disabled {
		cursor: not-allowed;
		pointer-events: none;
		opacity: 0.4;
	}
	a.orange {
		border-color: #fc7d2d;
		background-color: #fc7d2d;
	}
	a.deep-sea {
		border-color: #145d99;
		background-color: #145d99;
	}
	a.turquoise {
		border-color: #0CA6C7;
		background-color: #0CA6C7;
	}
	a.tangerine-hover {
		border-color: #f9663a;
		background-color: #f9663a;
	}
	a.tangerine-hover:hover {
		border-color: #ff7900;
		background-color: #ff7900;
	}
	a.tangerine-outline {
		border-color: #f9663a;
		color: #f9663a;
		background-color: #ffffff;
	}
	a.tangerine-outline:hover,
	a.tangerine-outline-transparent:hover {
		border-color: #ff7900;
		color: #ffffff;
		background-color: #ff7900;
	}
	a.tangerine-outline-transparent {
		border-color: #f9663a;
		color: #f9663a;
		background-color: transparent;
	}
	a.white {
		border-color: #441818;
		background-color: transparent;
		color: #441818;
	}
	a.none {
		border-color: transparent;
		background-color: transparent;
		color: inherit;
	}
</style>
