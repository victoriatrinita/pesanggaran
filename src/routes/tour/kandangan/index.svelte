<script>
	import ArticlesGrid from '../../../components/articles/ArticlesGrid.svelte';
	import Footer from '../../../components/Footer.svelte';
	import CoverCarousel from '../../../components/home/CoverCarousel.svelte';
	import PhotoCarousel from '../../../components/PhotoCarousel.svelte';
	import DescKandangan from '../../../components/tour/DescKandangan.svelte';
</script>

<CoverCarousel title={'Discover Kandangan'} />
<DescKandangan />
<PhotoCarousel title={'Must See'} higlightedTitle={'Attractions'} />
<ArticlesGrid />
<Footer />
