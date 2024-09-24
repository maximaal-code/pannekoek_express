<script lang="ts">
	import '../app.css'
	import { Navbar, NavBrand, NavLi, NavUl, NavHamburger } from 'flowbite-svelte'
</script>

<Navbar>
	<NavBrand href="/">
		<img src="/pancakes-svgrepo-com.svg" class="me-3 h-6 sm:h-9" alt="Pancake Express logo" />
		<!-- <div class="mr-2 h-10 w-10 overflow-hidden rounded-full">
			<img src="/truck_logo2.webp" class="scale-125 transform" alt="Pannekoek Express Logo" />
		</div> -->
		<!-- <img src="/flowbite-svelte-icon-logo.svg" class="me-3 h-6 sm:h-9" alt="Flowbite Logo" /> -->
		<span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white"
			>Pancake Express</span
		>
	</NavBrand>
	<div class="flex md:order-2">
		<NavHamburger />
	</div>
	<NavUl>
		<NavLi href="/">Over</NavLi>
		<NavLi href="/menu">Menu</NavLi>
		<NavLi href="/spoor">Volg het spoor</NavLi>
		<NavLi href="/contact">Contact</NavLi>
	</NavUl>
</Navbar>

<slot></slot>
