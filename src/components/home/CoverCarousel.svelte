<script>
	import Carousel from '@beyonk/svelte-carousel';
	import Link from '../Link.svelte';
	export let title, button, coverPhotos;
</script>

<main>
	<div>
		<h1>{title}</h1>
		{#if button}
		<Link href="gallery" color="turquoise" disabled>Get to Know Pesanggaran</Link>
		{/if}

	</div>

	<Carousel perPage={1} autoplay={5e3} duration={1e3}>
		{#each coverPhotos as coverPhoto}
		<section>
			<img src={coverPhoto.src} alt="Pesanggaran" />
			<p>Location</p>
		</section>
		{/each}
	</Carousel>
</main>

<style>
	h1 ~ :global(a) {
		font-size: 1.25rem;
	}

	img {
		height: 100%;
		width: 100%;
		object-fit: contain;
	}
	main :global(.carousel .slides) {
		height: 82vh;
	}
	main :global(.carousel ul) {
		padding-top: 2.5em;
	}
	main :global(.carousel) {
		padding-bottom: 2.5em;
	}
	main :global(.carousel li) {
		cursor: pointer;
		width: 1em;
		height: 1em;
		background-color: var(--t-gray);
	}
	main :global(.carousel li.active) {
		cursor: pointer;
		background-color: var(--p-blue);
	}

	section {
		position: relative;
	}
	p {
		bottom: 1%;
		left: 3%;
		position: absolute;
		font-weight: 600;
		color: #ffff;
		z-index: 1;
	}

	h1 {
		background-image: url();
		text-align: center;
		font-weight: 700;
		font-size: 3rem;
		color: #ffff;
		filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.25));
	}
	main {
		display: flex;
		justify-content: center;
		padding: 0 6em;
	}
	main > div {
		position: absolute;
		z-index: 1;
		text-align: center;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);
	}
</style>
