<script>
	export let post;
</script>

<a href="article/{post.slug}">
	<div class="article-card" data-aos="fade-up">
		<div class="article-image">
			<img src={post.photo} alt="Article" />
		</div>
		<div class="article-detail">
			<p class="date">
				{post.date_published}
			</p>
			<h3>{post.title}</h3>
			<p class="description">{post.html}</p>
		</div>
	</div>
</a>

<style>
	.article-card {
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
	.article-card:hover {
		box-shadow: 0px 3.4359px 38px rgba(0, 0, 0, 0.2);
		transform: translateY(-0.5em);
	}
	.article-card:hover .article-detail h3 {
		color: var(--p-turquoise);
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
	.article-detail {
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
    p, h3 {
        margin: 0;
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
		.article-card {
			margin: 0 auto;
			width: 17.5em;
		}
	}

	@media only screen and (max-width: 320px) {
		.article-card {
			margin: 0 auto;
			width: 15em;
		}
	}
</style>
