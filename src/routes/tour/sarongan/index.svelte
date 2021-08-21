<script>
	import ArticlesGrid from '../../../components/articles/ArticlesGrid.svelte';
	import Footer from '../../../components/Footer.svelte';
	import CoverCarousel from '../../../components/home/CoverCarousel.svelte';
	import PhotoCarousel from '../../../components/PhotoCarousel.svelte';
	import DescSarongan from '../../../components/tour/DescSarongan.svelte';
</script>

<CoverCarousel title={'Discover Sarongan'} />
<DescSarongan />
<PhotoCarousel title={'Must See'} higlightedTitle={'Attractions'} />
<ArticlesGrid />
<Footer />
