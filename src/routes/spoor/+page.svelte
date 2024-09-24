<script>
	// Dummy data voor komende locaties
	const upcomingLocations = [
		{ datum: '12 oktober', locatie: 'Groningen Centraal', tijd: '10:00 - 18:00' },
		{ datum: '14 oktober', locatie: 'Amsterdam Centraal', tijd: '11:00 - 19:00' },
		{ datum: '16 oktober', locatie: 'Amesfoort Centraal', tijd: '12:00 - 20:00' },
		{ datum: '20 oktober', locatie: 'Hoorn kersenboogerd station', tijd: '12:00 - 20:00' }
	]

	// Actuele locatie - hier kun je een live locatie van Google Maps integreren
	const currentLocation = 'Het clubhuis 🏟️'

	const openGoogleMaps = () => {
		// Deze functie stuurt de gebruiker naar Google Maps voor routebeschrijvingen
		window.open('https://www.google.com/maps', '_blank')
	}

	// import { GoogleMap, Marker } from 'svelte-google-maps'
	// let currentLatLng = { lat: 51.9225, lng: 4.47917 } // Coördinaten van Rotterdam Centraal
</script>

<div class="min-h-screen bg-gray-50 py-12">
	<div class="mx-auto max-w-7xl px-4">
		<!-- Huidige locatie sectie -->
		<section class="mb-16 text-center">
			<h2 class="mb-4 text-4xl font-bold text-gray-800">
				Op welk station stopt Pancake Express vandaag?
			</h2>
			<p class="mb-6 text-lg text-gray-600">
				Volg onze route live en kom langs voor een heerlijke pannenkoek!
			</p>

			<!-- Live kaart sectie (vervang placeholder met Google Maps API later) -->
			<div class="flex h-64 w-full items-center justify-center rounded-lg bg-gray-300">
				<p class="font-semibold text-gray-700">[Google Maps Placeholder]</p>
				<!-- <GoogleMap {currentLatLng} zoom="14" apiKey={YOUR_GOOGLE_MAPS_API_KEY} class="h-64 w-full">
					<Marker {currentLatLng} />
				</GoogleMap> -->
			</div>

			<div class="mt-4">
				<h3 class="text-2xl font-semibold text-gray-800">Huidige locatie: {currentLocation}</h3>
				<button
					on:click={openGoogleMaps}
					class="mt-6 rounded-lg bg-blue-500 px-8 py-3 text-white transition duration-300 hover:bg-blue-600"
				>
					Kom langs!
				</button>
			</div>
		</section>

		<!-- Komende stops -->
		<section class="mb-16">
			<h2 class="mb-8 text-3xl font-semibold text-gray-800">Komende Stops</h2>
			<div class="rounded-lg bg-white p-6 shadow-lg">
				<table class="w-full text-left">
					<thead>
						<tr class="bg-gray-200">
							<th class="p-4 font-semibold text-gray-600">Datum</th>
							<th class="p-4 font-semibold text-gray-600">Locatie</th>
							<th class="p-4 font-semibold text-gray-600">Tijd</th>
						</tr>
					</thead>
					<tbody>
						{#each upcomingLocations as stop}
							<tr>
								<td class="border-t p-4 text-gray-600">{stop.datum}</td>
								<td class="border-t p-4 text-gray-600">{stop.locatie}</td>
								<td class="border-t p-4 text-gray-600">{stop.tijd}</td>
							</tr>
						{/each}
					</tbody>
				</table>
			</div>
		</section>

		<!-- Social media feed (Instagram/Twitter) -->
		<section class="mb-16">
			<h2 class="mb-8 text-3xl font-semibold text-gray-800">Volg ons op social media</h2>
			<div class="flex flex-col md:flex-row md:space-x-8">
				<!-- Instagram feed -->
				<div class="flex-1 rounded-lg bg-white p-6 text-center shadow-lg">
					<h3 class="mb-4 text-2xl font-semibold">Instagram</h3>
					<div class="flex h-64 w-full items-center justify-center rounded-lg bg-gray-300">
						<p class="font-semibold text-gray-700">[Instagram Feed Placeholder]</p>
					</div>
					<a
						href="https://www.instagram.com"
						target="_blank"
						class="mt-4 block text-blue-500 hover:underline"
					>
						Bekijk onze Instagram
					</a>
				</div>

				<!-- Twitter feed -->
				<div class="mt-8 flex-1 rounded-lg bg-white p-6 text-center shadow-lg md:mt-0">
					<h3 class="mb-4 text-2xl font-semibold">Twitter</h3>
					<div class="flex h-64 w-full items-center justify-center rounded-lg bg-gray-300">
						<p class="font-semibold text-gray-700">[Twitter Feed Placeholder]</p>
					</div>
					<a
						href="https://www.twitter.com"
						target="_blank"
						class="mt-4 block text-blue-500 hover:underline"
					>
						Bekijk onze Twitter
					</a>
				</div>
			</div>
		</section>
	</div>
</div>
