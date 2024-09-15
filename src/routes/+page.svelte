<script lang="ts">
	import { Alert } from 'flowbite-svelte'

	import { Banner, Skeleton, ImagePlaceholder } from 'flowbite-svelte'
	import { SalePercentSolid, ArrowRightOutline } from 'flowbite-svelte-icons'

	import { Carousel } from 'flowbite-svelte'

	import images from '$lib/images.json'

	const duration = 3000
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

	<Carousel {images} let:Controls>
		<Controls />
	</Carousel>

	<Skeleton class="py-4" />
	<ImagePlaceholder class="py-4" />

	<Alert>
		<span class="font-medium">Info alert!</span>
		Change a few things up and try submitting again.
	</Alert>
</div>
