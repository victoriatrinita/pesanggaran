<main>
	<h1>Discover the <span> Best of Pesanggaran</span></h1>
	<div>
		<a href="gallery">
			<div class="insight-card" data-aos="fade-up">
				<img src="photos/pantai-rajegwesi.jpg" alt="Beaches" />
				<p>Beaches</p>
			</div>
		</a>

		<a href="gallery">
			<div class="insight-card" data-aos="fade-up">
				<img src="photos/highland.jpg" alt="Highlands" />
				<p>Highlands</p>
			</div>
		</a>

		<a href="gallery">
			<div class="insight-card" data-aos="fade-up">
				<img src="photos/penyu-sukamade.jpg" alt="Flora and Fauna" />
				<p>Flora and Fauna</p>
			</div>
		</a>
	</div>
</main>

<style>
	h1 > span {
		color: #0ca6c7;
	}
	h1 {
		font-size: clamp(1.25rem, 3vw, 2.5rem);
		font-weight: 700;
		text-align: center;
	}
	main {
		padding: 2.5em 6em;
	}
	h1 ~ div {
		display: flex;
		justify-content: center;
		padding-top: 1.5em;
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

	a {
		margin: 0 2em;
		text-decoration: none;
	}

	p {
		text-align: center;
		font-weight: 500;
	}
	.insight-card {
		display: grid;
		align-content: center;
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
</style>
