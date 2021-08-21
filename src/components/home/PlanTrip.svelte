<div class="plan-trip">
	<img src="assets/plan-trip.jpg" alt="Plan Trip Now" />
	<div class="plan-trip-detail">
        <p>Enthusiastic, aren't you?</p>
		<h1>
			Plan
			<span>Your Trip Now !</span>
		</h1>
	</div>
</div>

<style>
	.plan-trip {
		display: flex;
		margin: 0 auto;
		justify-content: center;
		align-items: center;
		gap: 2em;
		padding: 2em;
	}
	img {
		width: 15%;
	}
	h1 {
		color: #333333;
		font-weight: 700;
		font-size: clamp(1.25rem, 3vw, 3.75rem);
		margin-bottom: 1em;
	}
	h1 ~ :global(a) {
		padding: 0.75em 1.375em;
	}
	span {
		color: var(--p-turquoise);
	}

	@media only screen and (max-width: 600px) {
		.plan-trip {
			flex-direction: column;
		}
		img {
			width: 20%;
		}
		h1 {
			text-align: center;
		}
		h1 ~ :global(a) {
			font-size: 0.625rem;
			padding: 0.9em 2.9em;
		}
		.plan-trip-detail {
			display: grid;
			margin: 0 auto;
			justify-content: center;
		}
	}
</style>

