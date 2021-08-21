<script>
	let values = [
		'Art of nature',
		'A quick escape from the city',
		'Leisure time with pleasure experience',
		'Beaches and Island at your disposal',
		'Journey to peace',
		'Feel the local’s warmth',
	];
</script>

<main>
	<h1>Our <span>Values</span></h1>

	<div>
		{#each values as value, id}
			<div>
				<h3>{id + 1}</h3>
				<p>{value}</p>
			</div>
		{/each}
	</div>
</main>

<style>
	h1 > span,
	h3 {
		color: #0ca6c7;
	}
	h1 {
		font-size: clamp(1.25rem, 3vw, 2.5rem);
		font-weight: 700;
		text-align: center;
	}
	h3 {
		font-weight: 700;
	}
	main {
		background: #f5f9fe;
		padding: 2.5em;
	}
	h1 ~ div:first-of-type {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(5em, 1fr));
		grid-gap: 1rem;
		align-items: center;
		justify-content: center;
		padding: 2em 0;
	}
	h1 ~ div:first-of-type > div {
		justify-items: center;
		height: 100%;
	}
	p {
		text-align: center;
	}
	div > div {
		display: grid;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}
</style>
