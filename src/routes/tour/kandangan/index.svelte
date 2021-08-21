<script>
	import ArticlesGrid from '../../../components/articles/ArticlesGrid.svelte';
	import Footer from '../../../components/Footer.svelte';
	import CoverCarousel from '../../../components/home/CoverCarousel.svelte';
	import PhotoCarousel from '../../../components/PhotoCarousel.svelte';
	import DescKandangan from '../../../components/tour/DescKandangan.svelte';

	const coverPhotos = [
		{ src: 'assets/slide1.jpg' },
		{ src: 'assets/slide2.jpg' },
		{ src: 'photos/kandangan-rumah-apung.jpg' },
	];

    const photos = [
		{ src: 'photos/teluk-damai.jpg' },
		{ src: 'photos/teluk-hijau-2.jpg' },
		{ src: 'photos/kandangan-rumah-apung.jpg' },
		{ src: 'photos/sukamade-pantai.jpg' },
		{ src: 'photos/highland.jpg' },
	];

</script>

<CoverCarousel title={'Discover Kandangan'} {coverPhotos}/>
<DescKandangan />
<PhotoCarousel title={'Must See'} higlightedTitle={'Attractions'} {photos}/>
<ArticlesGrid />
<Footer />
