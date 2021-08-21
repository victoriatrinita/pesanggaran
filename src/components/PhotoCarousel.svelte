<script>
	import Carousel from '@beyonk/svelte-carousel';
	import { ChevronLeftIcon, ChevronRightIcon } from 'svelte-feather-icons';
	import Link from './Link.svelte';
	import PhotoCard from './PhotoCard.svelte';
	export let title, higlightedTitle, photos;
</script>

<main class="photoCarousel">
	<h1>{title} <span>{higlightedTitle}</span></h1>
	<Carousel perPage={3} dots={false} autoplay={0} controls>
		<div class="control" slot="left-control">
			<ChevronLeftIcon />
		</div>
		<div class="control" slot="right-control">
			<ChevronRightIcon />
		</div>
		<!-- <div>
			{#await post('insight/filter-insight', {}) then { data }}
				{#each data
					.sort((x, y) => x.id - y.id)
					.slice(-3)
					.reverse() as insight}
					<InsightCard {insight} />-->
		{#each photos as photo}
			<section>
				<PhotoCard {photo} />
			</section>
		{/each}
		<!--
				{/each}
			{/await}
		</div> -->
	</Carousel>
	<div>
		<Link href="gallery" color="deep-sea">See More</Link>
	</div>
</main>

<style>
	/* :global(.slides > .button) {
		background-color: var(--s-blue);
		border-radius: 50%;
		height: 3em;
	} */
	.photoCarousel :global(button.right) {
		right: -10px;
	}
	.photoCarousel :global(button.left) {
		left: -10px;
	}
	.control {
		color: var(--p-gray);
		width: 100%;
		height: 70%;
		background-color: var(--s-blue);
		border-radius: 50%;
	}

	/* .control > div {
		background-color: var(--s-blue);
		border-radius: 50%;
		height: 1em;
	} */
	h1 > span {
		color: #0ca6c7;
	}
	h1 {
		font-size: clamp(1.25rem, 3vw, 2.5rem);
		text-align: center;
		font-weight: 700;
		padding-bottom: 0.8em;
	}
	main {
		padding: 2.5em 6em;
	}
	/* div:first-of-type {
		padding: 0 6em;
	} */
	main > div {
		padding: 2em 0 3em;
	}
	section {
		display: flex;
		align-items: center;
		justify-content: center;
	}
	main > div {
		display: flex;
		align-items: center;
		justify-content: center;
	}
</style>
