<script lang="ts">
	export let status = 404
	export let error = { message: 'womp womp' }
</script>

<div class="error-container">
	<h1>Oeps, Je hebt de trein gemist!</h1>

	<!-- Oeps afbeelding -->
	<img
		src="https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fthumbs.dreamstime.com%2Fz%2Fasian-depressed-traveler-waiting-train-station-mistakes-69128402.jpg&f=1&nofb=1&ipt=57f1a7493ed426a6d73d5d515ff71d7618700c114a124ee01d8e45e548832825&ipo=images"
		alt="Oeps, Je hebt de trein gemist!"
		class="error-image"
	/>

	<!-- Status code en foutmelding -->
	<p class="status">Error {status}</p>
	<p class="error-message">{error.message ?? 'Er ging iets mis, probeer het later opnieuw.'}</p>

	<!-- Home link -->
	<a href="/" style="text-decoration: none;">
		<button>Ga terug naar de homepage</button>
	</a>
</div>

<style>
	.error-container {
		text-align: center;
		padding: 4rem;
		font-family: Arial, sans-serif;
	}
	h1 {
		font-size: 4rem;
		color: #ff6600;
	}
	p {
		font-size: 1.5rem;
		margin-bottom: 2rem;
	}
	.error-image {
		max-width: 300px;
		margin: 0 auto;
		margin-bottom: 2rem;
	}
	.status {
		font-size: 2rem;
		color: #ff4500;
	}
	.error-message {
		font-size: 1.2rem;
	}
</style>
