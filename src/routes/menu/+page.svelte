<script>
	// Dummy data voor menu items
	const menuItems = {
		zoet: [
			{
				naam: 'De Klapper van de Klapperboom',
				beschrijving: 'Pannenkoek met kokos, Nutella en aardbeien.',
				prijs: '€7,50',
				afbeelding: 'https://via.placeholder.com/300x200' // Vervang dit met echte afbeelding
			},
			{
				naam: 'De Chocolade Express',
				beschrijving: 'Met een overvloed aan chocoladesaus, bananen en slagroom.',
				prijs: '€8,00',
				afbeelding: 'https://via.placeholder.com/300x200'
			},
			{
				naam: 'De Zoete Wagon',
				beschrijving: 'Pannenkoek met blauwe bessen, ahornsiroop en een bolletje vanille-ijs.',
				prijs: '€8,50',
				afbeelding: 'https://via.placeholder.com/300x200'
			}
		],
		hartig: [
			{
				naam: 'De Stoere Conducteur',
				beschrijving: 'Pannenkoek met spek, kaas en champignons.',
				prijs: '€9,00',
				afbeelding: 'https://via.placeholder.com/300x200'
			},
			{
				naam: 'De Lokomotief Burger',
				beschrijving: 'Pannenkoek gevuld met gehakt, kaas en barbecue-saus.',
				prijs: '€9,50',
				afbeelding: 'https://via.placeholder.com/300x200'
			},
			{
				naam: 'De Spoorchef',
				beschrijving: 'Spinazie, feta en tomaat voor de liefhebbers van iets gezonds.',
				prijs: '€8,50',
				afbeelding: 'https://via.placeholder.com/300x200'
			}
		],
		speciaal: [
			{
				naam: 'De Grand Tour',
				beschrijving:
					'Pannenkoek met geitenkaas, walnoten en honing (alleen deze maand beschikbaar!).',
				prijs: '€10,00',
				afbeelding: 'https://via.placeholder.com/300x200'
			}
		],
		kinderen: [
			{
				naam: 'Treintje Pannenkoek',
				beschrijving: 'Kleine pannenkoekjes met keuze uit verschillende toppings.',
				prijs: '€5,00',
				afbeelding: 'https://via.placeholder.com/300x200'
			}
		]
	}
</script>

<div class="min-h-screen bg-gray-50 py-12">
	<div class="mx-auto max-w-7xl px-4">
		<h1 class="mb-8 text-3xl font-semibold text-gray-800">Menu</h1>

		<!-- Categorie: Zoete Pannenkoeken -->
		<section class="mb-16">
			<h2 class="mb-8 text-3xl font-semibold text-gray-800">Treinwagon van de zoetekauw</h2>
			<div class="grid grid-cols-1 gap-8 md:grid-cols-2 lg:grid-cols-3">
				{#each menuItems.zoet as item}
					<div class="overflow-hidden rounded-lg bg-white shadow-lg">
						<img src={item.afbeelding} alt={item.naam} class="h-48 w-full object-cover" />
						<div class="p-6">
							<h3 class="text-xl font-bold text-gray-800">{item.naam}</h3>
							<p class="mt-2 text-gray-600">{item.beschrijving}</p>
							<p class="mt-4 text-lg font-semibold text-yellow-500">{item.prijs}</p>
						</div>
					</div>
				{/each}
			</div>
		</section>

		<!-- Categorie: Hartige Pannenkoeken -->
		<section class="mb-16">
			<h2 class="mb-8 text-3xl font-semibold text-gray-800">Het Station van de Hartenbrekers</h2>
			<div class="grid grid-cols-1 gap-8 md:grid-cols-2 lg:grid-cols-3">
				{#each menuItems.hartig as item}
					<div class="overflow-hidden rounded-lg bg-white shadow-lg">
						<img src={item.afbeelding} alt={item.naam} class="h-48 w-full object-cover" />
						<div class="p-6">
							<h3 class="text-xl font-bold text-gray-800">{item.naam}</h3>
							<p class="mt-2 text-gray-600">{item.beschrijving}</p>
							<p class="mt-4 text-lg font-semibold text-yellow-500">{item.prijs}</p>
						</div>
					</div>
				{/each}
			</div>
		</section>

		<!-- Categorie: Speciale Treinreizen -->
		<section class="mb-16">
			<h2 class="mb-8 text-3xl font-semibold text-gray-800">Speciale Treinreizen</h2>
			<div class="grid grid-cols-1 gap-8 md:grid-cols-2 lg:grid-cols-3">
				{#each menuItems.speciaal as item}
					<div class="overflow-hidden rounded-lg bg-white shadow-lg">
						<img src={item.afbeelding} alt={item.naam} class="h-48 w-full object-cover" />
						<div class="p-6">
							<h3 class="text-xl font-bold text-gray-800">{item.naam}</h3>
							<p class="mt-2 text-gray-600">{item.beschrijving}</p>
							<p class="mt-4 text-lg font-semibold text-yellow-500">{item.prijs}</p>
						</div>
					</div>
				{/each}
			</div>
		</section>

		<!-- Categorie: Kinderpannenkoeken -->
		<section class="mb-16">
			<h2 class="mb-8 text-3xl font-semibold text-gray-800">Kleine locomotiefjes</h2>
			<div class="grid grid-cols-1 gap-8 md:grid-cols-2 lg:grid-cols-3">
				{#each menuItems.kinderen as item}
					<div class="overflow-hidden rounded-lg bg-white shadow-lg">
						<img src={item.afbeelding} alt={item.naam} class="h-48 w-full object-cover" />
						<div class="p-6">
							<h3 class="text-xl font-bold text-gray-800">{item.naam}</h3>
							<p class="mt-2 text-gray-600">{item.beschrijving}</p>
							<p class="mt-4 text-lg font-semibold text-yellow-500">{item.prijs}</p>
						</div>
					</div>
				{/each}
			</div>
		</section>

		<!-- Call-to-action -->
		<section class="py-12 text-center">
			<h2 class="text-3xl font-bold text-gray-800">Bestellen?</h2>
			<p class="mt-4 text-lg text-gray-600">
				Plaats je bestelling bij de truck of neem contact met ons op voor grotere bestellingen!
			</p>
		</section>
	</div>
</div>
