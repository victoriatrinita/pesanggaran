<script context="module">
	export function preload() {
		return this.fetch(`article.json`)
			.then((r) => r.json())
			.then((posts) => {
				return { posts };
			});
	}
</script>

<script>
	import Footer from '../../components/Footer.svelte';
	import ArticleCard from '../../components/articles/ArticleCard.svelte';

	const posts = [
		{
			title: 'Liburan dengan Tetap di Rumah? Bisa, dan Tetap Seru dengan Berwisata Online?',
			slug: 'liburan-dengan-tetap-di-rumah-bisa-dan-tetap-seru-dengan-berwisata-online',
			date_published: '16 August, 2021',
			photo: 'https://i.imgur.com/EWjLPEH.png',
			html: 'Indeed, at this time it is not an easy matter to stay at home and limit activities outside ...',
		},
		{
			title: 'Here are 5 beautiful beaches in Sarongan that you must visit!',
			slug: '5-beautiful-beaches-in-sarongan-that-you-must-visit',
			date_published: '14 August, 2021',
			photo: 'https://i.imgur.com/yIp7ZbV.jpg',
			html: 'Sarongan Village, Pesanggaran District presents a holiday atmosphere in the open which is ...',
		},
		{
			title: "Can't Go on a vacation yet? Make a Travel Plan First",
			slug: 'cant-go-on-a-vacation-yet-make-a-travel-plan-first',
			date_published: '11 August, 2021',
			photo:
				'https://images.unsplash.com/photo-1615826932727-ed9f182ac67e?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1351&q=80',
			html: 'Indeed, conditions like today are not yet possible for us to spend time at tourist attractions ...',
		},
		{
			title: 'Teluk Hijau (Green Bay) : Beautiful Secluded Hidden Beach',
			slug: 'teluk-hijau-green-bay-beautiful-secluded-hidden-beach',
			date_published: '9 August, 2021',
			photo: 'https://i.imgur.com/sH3HYHv.jpg',
			html: 'Located about 90 km on the south of the city of Banyuwangi, Teluk Hijau sits on the area of ...',
		},
	];
</script>

<svelte:head>
	<title>Blog</title>
</svelte:head>

<section>
	<h1>Recent posts</h1>

	<div>
		{#each posts.sort((x, y) => x.id - y.id).reverse() as post}
			<ArticleCard {post} />
		{/each}
	</div>

	<Footer />
</section>

<style>
	div {
		width: 100%;
		display: grid;
		gap: 3em;
		justify-content: center;
		grid-template-columns: repeat(auto-fit, minmax(20em, auto));
		margin-bottom: 10em;
	}

	section {
		padding: 2.5em;
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
