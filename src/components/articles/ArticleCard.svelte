<script>
	export let insight;
</script>

<a href="insights/{insight.id}">
	<div class="insight-card" data-aos="fade-up">
		<div class="insight-image">
			<img src={insight.image} alt="Insights" />
		</div>
		<div class="insight-detail">
			<p class="date">
				{new Date(insight.date_posted).toUTCString().split(' ').slice(0, -2).join(' ')}
			</p>
			<h3>{insight.title}</h3>
			<p class="description">{insight.overview}</p>
		</div>
	</div>
</a>

<style>
	.insight-card {
		display: grid;
		gap: 1em;
		align-content: flex-start;
		background-color: #ffffff;
		width: 20em;
		height: 100%;
		cursor: pointer;
		box-shadow: 0px 3px 17px rgba(0, 0, 0, 0.14);
		transition: all 300ms ease-out;
	}
	.insight-card:hover {
		box-shadow: 0px 3.4359px 38px rgba(0, 0, 0, 0.2);
		transform: translateY(-0.5em);
	}
	.insight-card:hover .insight-detail h3 {
		color: #fb6b13;
	}
	img {
		width: 100%;
		height: 100%;
		object-fit: cover;
		max-height: 12em;
		top: 0;
		left: 0;
		text-align: center;
	}
	.insight-detail {
		display: grid;
		flex-direction: column;
		padding: 0.5em 1em;
		margin-bottom: 0.5em;
		gap: 0.625em;
	}
	p.date {
		font-size: 0.75rem;
		color: #b1b1b1;
	}
	a {
		text-decoration: none;
	}
	h3 {
		color: #000000;
		font-size: 1rem;
		font-weight: 500;
		line-height: 1.5em;
		transition: 300ms;
	}
	p.description {
		color: #666666;
		font-size: 0.875rem;
	}

	@media only screen and (max-width: 375px) {
		.insight-card {
			margin: 0 auto;
			width: 17.5em;
		}
	}

	@media only screen and (max-width: 320px) {
		.insight-card {
			margin: 0 auto;
			width: 15em;
		}
	}
</style>
