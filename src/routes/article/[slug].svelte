<script context="module">
	export async function preload({ params }) {
		// the `slug` parameter is available because
		// this file is called [slug].svelte
		const res = await this.fetch(`article/${params.slug}.json`);
		const data = await res.json();

		if (res.status === 200) {
			return { post: data };
		} else {
			this.error(res.status, data.message);
		}
	}
</script>

<script>
	export let post;
	import Footer from '../../components/Footer.svelte'
</script>

<svelte:head>
	<title>{post.title}</title>
</svelte:head>

<article>
	<p>Published {post.date_published}</p>
	<h1>{post.title}</h1>

	<div class="content">
		{@html post.html}
	</div>
</article>

<Footer />

<style>
	/*
		By default, CSS is locally scoped to the component,
		and any unused styles are dead-code-eliminated.
		In this page, Svelte can't know which elements are
		going to appear inside the {{{post.html}}} block,
		so we have to use the :global(...) modifier to target
		all elements inside .content
	*/
	article {
		padding: 2.5em 6em;
	}

	h1 {
		font-weight: 700;
		text-align: center;
		max-width: 84rem;
		width: 100%;
		padding: 0;
		margin: 0em auto 0.5em;
		text-align: center;
		font-size: clamp(1.25rem, 3vw, 2.5rem);
	}

	p {
		text-align: center;
		color: var(--s-gray);
	}

	.content {
		display: flex;
		flex-direction: column;
	}

	.content :global(h2) {
		font-size: 1.4em;
		font-weight: 500;
	}

	.content :global(pre) {
		background-color: #f9f9f9;
		box-shadow: inset 1px 1px 5px rgba(0, 0, 0, 0.05);
		padding: 0.5em;
		border-radius: 2px;
		overflow-x: auto;
	}

	.content :global(pre) :global(code) {
		background-color: transparent;
		padding: 0;
	}

	.content :global(p) {
		text-align: justify;
	}

	.content :global(ul) {
		line-height: 1.5;
	}

	.content :global(li) {
		margin: 0 0 0.5em 0;
	}

	.content :global(img) {
		width: 40em;
		align-self: center;
	}

	.content :global(a) {
		color: var(--p-blue);
	}
</style>
