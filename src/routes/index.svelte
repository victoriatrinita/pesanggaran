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
</script>

<svelte:head>
	<title>Visit Kandangan & Sarongan</title>
</svelte:head>

<CoverCarousel title={'Spark Your Wanderlust'} button {coverPhotos} />
<OurStory />
<Discover />
<PhotoCarousel title={'Favourite'} higlightedTitle={'Destinations'} />
<ArticlesGrid />
<DiveFurther />
<PlanTrip />
<Footer />
