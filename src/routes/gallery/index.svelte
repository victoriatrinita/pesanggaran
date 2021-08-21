<script>
	import Footer from '../../components/Footer.svelte';

	const photos = [
		{ src: 'https://i.imgur.com/cmSCHEO.jpg' },
		{ src: 'photos/penyu-hijau.jpg' },
		{ src: 'photos/kandangan-rumah-apung.jpg' },
		{ src: 'photos/sarongan-pantai-batu-1.jpg' },
		{ src: 'photos/pantai-permisan.jpg' },
		{ src: 'photos/pantai-rajegwesi.jpg' },
		{ src: 'https://i.imgur.com/wxyXWgM.jpg' },
		{ src: 'https://i.imgur.com/4KF5SQE.jpg' },
		{ src: 'https://i.imgur.com/HFRVtGk.jpg' },
		{ src: 'https://i.imgur.com/uNjmOeo.jpg' },
		{ src: 'https://i.imgur.com/wNetkwM.jpg' },
		{ src: 'https://i.imgur.com/G0lT4Vq.jpg' },
		{ src: 'https://i.imgur.com/bvw3nwX.jpg' },
		{ src: 'https://i.imgur.com/FFt55YO.jpg' },
		{ src: 'https://i.imgur.com/M6ioBQx.jpg' },
		{ src: 'https://i.imgur.com/JicAusJ.jpg' },
		{ src: 'https://i.imgur.com/4UtaoFd.jpg' },
		{ src: 'https://i.imgur.com/whB55Bj.jpg' },
		{ src: 'https://i.imgur.com/AKLnuP4.jpg' },
		{ src: 'https://i.imgur.com/EIHGpQL.jpg' },
		{ src: 'https://i.imgur.com/cIXLqLL.jpg' },
		{ src: 'https://i.imgur.com/yni8NHU.jpg' },
		{ src: 'https://i.imgur.com/UA6ZWnr.jpg' },
		{ src: 'https://i.imgur.com/YJLmjft.jpg' },
		{ src: 'https://i.imgur.com/aNJV3Tt.jpg' },
		{ src: 'https://i.imgur.com/YJZdEu2.jpg' },
		{ src: 'https://i.imgur.com/TzFBZyb.jpg' },
		{ src: 'https://i.imgur.com/GKsTpNr.jpg' },
		{ src: 'https://i.imgur.com/8zVjyDN.jpg' },
		{ src: 'https://i.imgur.com/HYR6ueV.jpg' },
		{ src: 'photos/teluk-damai.jpg' },
		{ src: 'photos/teluk-hijau-2.jpg' },
		{ src: 'photos/sukamade-pantai.jpg' },
	];
</script>

<section>
	<div>
		{#each photos.sort((x, y) => x.id - y.id) as photo}
			<div class="gallery-card" data-aos="fade-up">
				<div class="article-image">
					<img src={photo.src} alt="Article" />
				</div>
			</div>
		{/each}
	</div>
</section>

<Footer />

<style>
	section {
		padding: 2.5em;
		background-color: #f5f9fe;
	}
	div {
		width: 100%;
		display: grid;
		gap: 3em;
		justify-content: center;
		grid-template-columns: repeat(auto-fit, minmax(20em, auto));
	}
	.gallery-card {
		display: grid;
		gap: 1em;
		align-content: flex-start;
		background-color: #ffffff;
		width: 20em;
		height: 100%;
		/* cursor: pointer; */
		box-shadow: 0px 3px 17px rgba(0, 0, 0, 0.14);
		transition: all 300ms ease-out;
	}
	.gallery-card:hover {
		box-shadow: 0px 3.4359px 38px rgba(0, 0, 0, 0.2);
		transform: translateY(-0.5em);
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

	@media only screen and (max-width: 768px) {
		div {
			gap: 1.5em;
		}
	}

	@media only screen and (max-width: 375px) {
		.gallery-card {
			margin: 0 auto;
			width: 17.5em;
		}
	}

	@media only screen and (max-width: 320px) {
		.gallery-card {
			margin: 0 auto;
			width: 15em;
		}
	}
</style>
