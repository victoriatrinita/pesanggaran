<script>
	export let segment;
	import { stores } from '@sapper/app';
	const { page } = stores();
	$: check = (current) => ($page.path.startsWith(current) ? 'page' : undefined);
</script>

<nav>
	<img src="assets/logo.png" alt="logo" href="." />

	<ul>
		<li>
			<a aria-current={segment === undefined ? 'page' : undefined} href=".">Home</a>
		</li>
		<li>
			<a aria-current={segment === 'about' ? 'page' : undefined} href="about">About</a>
		</li>
		<li>
			<a aria-current={segment === 'gallery' ? 'page' : undefined} href="gallery">Gallery</a>
		</li>
		<!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
		the blog data when we hover over the link or tap it on a touchscreen -->
		<li>
			<a rel="prefetch" aria-current={segment === 'article' ? 'page' : undefined} href="article"
				>Article</a
			>
		</li>
		<li>
			<a aria-current={check('/tour/kandangan')} href="tour/kandangan">Tour Kandangan</a>
		</li>
		<li>
			<a aria-current={check('/tour/sarongan')} href="tour/sarongan">Tour Sarongan</a>
		</li>
	</ul>
</nav>

<style>
	a {
		font-size: 1.25rem;
	}

	nav {
		font-weight: bold;
		padding: 1em 5em;
		display: flex;
		justify-content: space-between;
		align-items: flex-end;
	}

	nav > img {
		width: 17em;
		cursor: pointer;
	}

	ul {
		margin: auto 0;
	}

	ul::after {
		content: '';
		display: block;
		clear: both;
	}

	li {
		display: block;
		float: left;
	}

	[aria-current] {
		position: relative;
		display: inline-block;
	}

	[aria-current]::after {
		position: absolute;
		content: '';
		width: calc(100% - 2em);
		height: 0.1em;
		background-color: #0ca6c7;
		display: block;
		bottom: -1px;
	}

	a {
		text-decoration: none;
		padding: 0 1em;
		display: block;
	}
</style>
