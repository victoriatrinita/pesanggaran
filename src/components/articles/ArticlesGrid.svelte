<script>
	import ArticleCard from './ArticleCard.svelte';
	import Link from '../Link.svelte';
	const data = [
		{
			id: 1,
			image: 'assets/slide2.jpg',
			date_posted: '2 April',
			title: 'hello',
			overview: 'test test test test',
		},
		{
			id: 1,
			image: 'assets/slide2.jpg',
			date_posted: '2 April',
			title: 'hello',
			overview: 'test test test test',
		},
		{
			id: 1,
			image: 'assets/slide2.jpg',
			date_posted: '2 April',
			title: 'hello',
			overview: 'test test test test',
		},
	];
</script>

<section>
	<h1>Read <span>More</span></h1>

	<div>
		{#each data
			.sort((x, y) => x.id - y.id)
			.slice(-3)
			.reverse() as insight}
			<ArticleCard {insight} />
		{/each}
	</div>

	<div>
		<Link href="article" color="deep-sea">See More</Link>
	</div>
</section>

<style>
	div {
		width: 100%;
		display: grid;
		gap: 3em;
		justify-content: center;
		grid-template-columns: repeat(auto-fit, minmax(20em, auto));
	}

	section {
		padding: 2.5em;
		background-color: #f5f9fe;
	}
	h1 > span {
		color: #0ca6c7;
	}
	h1 {
		font-size: clamp(1.25rem, 3vw, 2.5rem);
		font-weight: 700;
		text-align: center;
	}
	div:nth-of-type(2) {
		margin: 2.5em auto 0;
		display: flex;
		align-items: center;
	}

	@media only screen and (max-width: 768px) {
		div {
			gap: 1.5em;
		}
	}
</style>
