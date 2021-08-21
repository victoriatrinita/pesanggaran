<script>
	import CoverCarousel from '../components/home/CoverCarousel.svelte';
	import Discover from '../components/home/Discover.svelte';
	import DiveFurther from '../components/home/DiveFurther.svelte';
	import OurStory from '../components/home/OurStory.svelte';
	import PlanTrip from '../components/home/PlanTrip.svelte';
	import Footer from '../components/Footer.svelte';
	import PhotoCarousel from '../components/PhotoCarousel.svelte';
	import ArticlesGrid from '../components/articles/ArticlesGrid.svelte';

	const coverPhotos = [
		{ src: 'photos/sukamade-pantai.jpg' },
		{ src: 'photos/teluk-hijau.jpg' },
		{ src: 'photos/penyu-hijau.jpg' },
	];

	const photos = [
		{ src: 'photos/teluk-damai.jpg' },
		{ src: 'photos/teluk-hijau-2.jpg' },
		{ src: 'photos/kandangan-rumah-apung.jpg' },
		{ src: 'photos/sarongan-pantai-batu-1.jpg' },
		{ src: 'photos/pantai-permisan.jpg' },
		{ src: 'photos/pantai-rajegwesi.jpg' },
	];

</script>

<svelte:head>
	<title>Visit Kandangan & Sarongan</title>
</svelte:head>

<CoverCarousel title={'Spark Your Wanderlust'} button {coverPhotos} />
<OurStory />
<Discover />
<PhotoCarousel title={'Favourite'} higlightedTitle={'Destinations'} {photos} />
<ArticlesGrid />
<DiveFurther />
<PlanTrip />
<Footer />
