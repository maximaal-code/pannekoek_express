<script lang="ts">
	import { Alert } from 'flowbite-svelte'

	import { Banner, Skeleton, ImagePlaceholder } from 'flowbite-svelte'
	import { SalePercentSolid, ArrowRightOutline } from 'flowbite-svelte-icons'
	import { Card } from 'flowbite-svelte'
	import { Carousel } from 'flowbite-svelte'

	import images from '$lib/images.json'
	import { goto } from '$app/navigation'

	const duration = 3000

	const viewMenu = () => {
		goto('/menu')
		console.log('Navigeren naar het menu')
	}

	const followLocation = () => {
		goto('spoor')
		console.log('Volg onze locatie')
	}
</script>

<div class="p-8">
	<Banner id="bottom-banner" position="absolute" bannerType="bottom">
		<p class="flex items-center text-sm font-normal text-gray-500 dark:text-gray-400">
			<span class="me-3 inline-flex rounded-full bg-gray-200 p-1 dark:bg-gray-600">
				<SalePercentSolid class="h-4 w-4 text-gray-500 dark:text-gray-400" />
				<span class="sr-only">Discount coupon</span>
			</span>
			<span>
				Get 5% commission per sale <a
					href="https://flowbite.com"
					class="ms-0 flex items-center text-sm font-medium text-primary-600 hover:underline md:ms-1 md:inline-flex dark:text-primary-500"
				>
					Become a partner <ArrowRightOutline class="ms-2 h-3 w-3" />
				</a>
			</span>
		</p>
	</Banner>

	<Carousel {images} {duration} let:Controls>
		<Controls />
	</Carousel>

	<!-- <article>
		<h1 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">
			Welkom op Pancake Express!
		</h1>
		<p>Stap aan boord van de lekkerste treinrit vol zoete en hartige avonturen!</p>
	</article> -->
</div>

<div class="flex min-h-screen flex-col bg-gray-50">
	<!-- Header -->
	<header class="bg-yellow-500 py-6 text-center text-white">
		<h1 class="text-4xl font-bold">Welkom op Pancake Express!</h1>
		<p class="mt-2 text-xl">
			"Stap aan boord van de lekkerste treinrit vol zoete en hartige avonturen!"
		</p>
	</header>

	<!-- Introductie-sectie -->
	<section class="flex flex-1 items-center justify-center py-12">
		<div class="max-w-3xl text-center">
			<p class="text-lg text-gray-700">
				Bij Pancake Express nemen we je mee op een culinaire reis door de wereld van pannenkoeken.
				Onze foodtruck, geïnspireerd door klassieke treinen, serveert de heerlijkste pannenkoeken:
				van zoet en fruitig tot hartig en vullend. Of je nu onderweg bent of een gezellige lunchplek
				zoekt, wij staan voor je klaar!
			</p>
			<div class="mt-8">
				<button
					on:click={viewMenu}
					class="mr-4 rounded-lg bg-yellow-500 px-6 py-3 text-white transition duration-300 hover:bg-yellow-600"
				>
					Bekijk Menu
				</button>
				<button
					on:click={followLocation}
					class="rounded-lg bg-blue-500 px-6 py-3 text-white transition duration-300 hover:bg-blue-600"
				>
					Volg onze Locatie
				</button>
			</div>
		</div>
	</section>

	<!-- Over ons-sectie -->
	<section class="bg-white py-12">
		<div class="mx-auto max-w-4xl text-center">
			<h2 class="text-3xl font-semibold text-gray-800">Over ons</h2>
			<p class="mt-6 text-lg text-gray-700">
				Pancake Express is geboren uit onze liefde voor zowel pannenkoeken als reizen. Wat begon als
				een klein idee, is nu uitgegroeid tot een unieke foodtruck die door het land toert. Bij ons
				krijg je niet alleen heerlijke pannenkoeken, maar ook een ervaring die je meeneemt naar de
				gouden dagen van treinreizen.
			</p>
		</div>
	</section>

	<!-- Testimonials-sectie -->
	<section class="bg-gray-100 py-12">
		<div class="mx-auto max-w-4xl text-center">
			<h2 class="text-3xl font-semibold text-gray-800">Wat onze klanten zeggen</h2>
			<div class="mt-8 space-y-6">
				<!-- Testimonial 1 -->
				<div class="rounded-lg bg-white p-6 shadow-lg">
					<p class="text-lg italic text-gray-700">
						"De beste pannenkoeken die ik ooit heb geproefd! En dat vanuit zo'n gezellige
						foodtruck."
					</p>
					<p class="mt-4 text-sm text-gray-500">– Sophie J.</p>
				</div>
				<!-- Testimonial 2 -->
				<div class="rounded-lg bg-white p-6 shadow-lg">
					<p class="text-lg italic text-gray-700">
						"Fantastische ervaring, van de heerlijke pannenkoeken tot het vriendelijke personeel!"
					</p>
					<p class="mt-4 text-sm text-gray-500">– Mark V.</p>
				</div>
				<!-- Testimonial 3 -->
				<div class="rounded-lg bg-white p-6 shadow-lg">
					<p class="text-lg italic text-gray-700">
						"Geweldige smaak en een unieke presentatie. Ik kan niet wachten om terug te komen!"
					</p>
					<p class="mt-4 text-sm text-gray-500">– Lisa K.</p>
				</div>
			</div>
		</div>
	</section>

	<!-- Footer -->
	<footer class="bg-gray-800 py-6 text-white">
		<div class="mx-auto max-w-4xl space-y-4 text-center">
			<h2 class="text-2xl font-semibold">Contactinformatie</h2>
			<p>
				E-mailadres: <a href="mailto:info@pancakeexpress.nl" class="text-yellow-400"
					>info@pancakeexpress.nl</a
				>
			</p>
			<p>Telefoon: <a href="tel:0612345678" class="text-yellow-400">0612345678</a></p>

			<div class="mt-4 flex justify-center space-x-6">
				<a
					href="https://facebook.com"
					target="_blank"
					class="transition duration-300 hover:text-yellow-400">Facebook</a
				>
				<a
					href="https://instagram.com"
					target="_blank"
					class="transition duration-300 hover:text-yellow-400">Instagram</a
				>
			</div>
		</div>
	</footer>
</div>
