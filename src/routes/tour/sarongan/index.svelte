<script>
	import ArticlesGrid from '../../../components/articles/ArticlesGrid.svelte';
	import Footer from '../../../components/Footer.svelte';
	import CoverCarousel from '../../../components/home/CoverCarousel.svelte';
	import PhotoCarousel from '../../../components/PhotoCarousel.svelte';
	import DescSarongan from '../../../components/tour/DescSarongan.svelte';

	const coverPhotos = [
		{ src: 'photos/sukamade-1.jpg' },
		{ src: 'photos/sukamade-2.jpg' },
		{ src: 'photos/teluk-hijau-2.jpg' },
	];

	const photos = [
		{ src: 'photos/teluk-damai.jpg' },
		{ src: 'photos/teluk-hijau-2.jpg' },
		{ src: 'photos/sukamade-pantai.jpg' },
		{ src: 'photos/sarongan-pantai-batu.jpg' },
		{ src: 'photos/pantai-permisan.jpg' },
	];
</script>

<CoverCarousel title={'Discover Sarongan'} {coverPhotos} />
<DescSarongan />
<PhotoCarousel title={'Must See'} higlightedTitle={'Attractions'} {photos} />
<ArticlesGrid />
<Footer />
