<script>
	import ArticlesGrid from '../../../components/articles/ArticlesGrid.svelte';
	import Footer from '../../../components/Footer.svelte';
	import CoverCarousel from '../../../components/home/CoverCarousel.svelte';
	import PhotoCarousel from '../../../components/PhotoCarousel.svelte';
	import DescSarongan from '../../../components/tour/DescSarongan.svelte';

	const coverPhotos = [
		{ src: 'assets/slide1.jpg' },
		{ src: 'assets/slide2.jpg' },
		{ src: 'assets/slide3.jpg' },
	];
</script>

<CoverCarousel title={'Discover Sarongan'} {coverPhotos} />
<DescSarongan />
<PhotoCarousel title={'Must See'} higlightedTitle={'Attractions'} />
<ArticlesGrid />
<Footer />
