<script lang="ts">
	import Search from 'lucide-svelte/icons/search';
	import MobileNavbar from './mobile-navbar.svelte';
	import ShoppingCart from 'lucide-svelte/icons/shopping-cart';
	import { onMount } from 'svelte';
	const isMobile =
		typeof window !== 'undefined' &&
		/Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent);
</script>
<header class="border-b-[1px] border-gray-200 pb-3s">

	<div class="w-screen bg-primary text-center uppercase text-secondary">
		<span>🛒 SvelteKit Shopping Cart</span>
	</div>

	<div class="mx-4 mt-3 flex items-center justify-around md:justify-center">
		<div class="flex items-center gap-3">
			<Search />
			<ShoppingCart />
		</div>
		<img src="/logo.svg" alt="logo" />
		<MobileNavbar />
	</div>

	<!-- <nav class="mx-12 flex items-center justify-center gap-12 border-b-[1px] border-gray-200">
		<a href="/">Home</a>
		<a href="/">Home</a>
		<a href="/about">About</a>
		<a href="/contact">Contact</a>
	</nav> -->
</header>
