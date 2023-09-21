<script>
	import Swiper from 'swiper';
	import { Navigation, Autoplay } from 'swiper/modules';
	import 'swiper/css';
	import 'swiper/css/navigation';
	import { onMount } from 'svelte';

	onMount(() => {
		new Swiper('.swiper', {
			direction: 'horizontal',
			loop: true,
			modules: [Navigation, Autoplay],
			autoplay: {
				delay: 5000,
				disableOnInteraction: false,
			},
			speed: 900,
		});
	});
</script>

<main class="relative w-screen h-screen bg-zinc-950">
	<div class="absolute w-screen h-screen swiper">
		<div class="swiper-wrapper">
			<div class="swiper-slide">
				<div class="img-container">
					<img src="/img-1.png" alt="background" />
					<div class="overlay" />
				</div>
			</div>
			<div class="swiper-slide">
				<div class="img-container">
					<img src="/img-2.png" alt="background" />
					<div class="overlay" />
				</div>
			</div>
			<div class="swiper-slide">
				<div class="img-container">
					<img src="/img-3.png" alt="background" />
					<div class="overlay" />
				</div>
			</div>
		</div>
	</div>

	<div
		class="absolute inset-0 select-none flex justify-center items-center px-6"
	>
		<div class="z-20 flex flex-col justify-center items-center relative">
			<div class="flex justify-center items-center gap-6">
				<img src="logo.webp" alt="logo" class="w-12 md:w-24" />
				<h1 class="text-2xl md:text-7xl w-fit">New York State Roleplay</h1>
			</div>
			<p class="mt-1 text-2xl text-center">
				Professional, creative, unique roleplay
			</p>

			<div class="flex gap-2 mt-4 links">
				<a href="https://discord.gg/nys" target="_blank">
					<img src="/discord.svg" alt="discord logo" class="w-7 md:w-10" />
				</a>
				<a href="https://twitter.com/NYSRP_1" target="_blank">
					<img
						src="/twitter.svg"
						alt="instagram logo"
						class="w-6 md:w-9 ml-2"
					/>
				</a>
			</div>
		</div>
	</div>
</main>
