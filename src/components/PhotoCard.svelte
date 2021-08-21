<script>
	export let photo;
</script>

<a href="articles">
	<div data-aos="fade-up">
		<div>
			<img src={photo.src} alt="destination" />
		</div>
	</div>
</a>

<style>
	a > div {
		display: grid;
		gap: 1em;
		align-content: flex-start;
		border-radius: 0.75em;
		background-color: #ffffff;
		width: 20em;
		height: 100%;
		cursor: pointer;
		box-shadow: 0px 3px 17px rgba(0, 0, 0, 0.14);
		transition: all 300ms ease-out;
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
		a > div {
			width: 100%;
			max-width: unset;
		}
	}
</style>
