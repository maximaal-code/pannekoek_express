<script lang="ts">
	export let status = 404
	export let error = { message: 'womp womp' }
</script>

<div class="flex min-h-screen flex-col items-center justify-center bg-gray-100 p-6 text-center">
	<h1 class="mb-6 text-2xl font-bold text-orange-600 sm:text-3xl lg:text-5xl">
		Oeps, Je hebt de trein gemist!
	</h1>

	<!-- Oeps afbeelding -->
	<img
		src="https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fthumbs.dreamstime.com%2Fz%2Fasian-depressed-traveler-waiting-train-station-mistakes-69128402.jpg&f=1&nofb=1&ipt=57f1a7493ed426a6d73d5d515ff71d7618700c114a124ee01d8e45e548832825&ipo=images"
		alt="Oeps, Je hebt de trein gemist!"
		class="mb-6 w-full max-w-sm rounded shadow-lg sm:max-w-md lg:max-w-3xl"
	/>

	<!-- Status code en foutmelding -->
	<p class="mb-4 text-xl text-red-600 sm:text-2xl">Error {status}</p>
	<p class="mb-8 text-base text-gray-700 sm:text-lg">
		{error.message ?? 'Er ging iets mis, probeer het later opnieuw.'}
	</p>

	<!-- Home link -->
	<a
		href="/"
		class="rounded-lg bg-blue-600 px-6 py-3 text-lg font-medium text-white hover:bg-blue-700 focus:ring-4 focus:ring-blue-300"
	>
		Ga terug naar de homepage
	</a>
</div>
