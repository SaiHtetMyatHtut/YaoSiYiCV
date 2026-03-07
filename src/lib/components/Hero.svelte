<script lang="ts">
	import { onMount } from 'svelte';

	const womanPhoto = 'https://www.figma.com/api/mcp/asset/73a2d19a-e55c-4c4d-8bed-d9a520b72c60';
	const ellipseOrange = 'https://www.figma.com/api/mcp/asset/31941aae-534b-4050-88d9-0f0b4167a9e4';
	const quoteIcon = 'https://www.figma.com/api/mcp/asset/7f6c6041-1b1d-46c2-9c25-5a555f532248';
	const starIcon = 'https://www.figma.com/api/mcp/asset/eb0296c5-33d2-40d0-88ce-afd0007be31d';
	const arrowIcon = 'https://www.figma.com/api/mcp/asset/6983c991-f0b3-42d3-93f7-d0035c31263f';
	const arrowIcon2 = 'https://www.figma.com/api/mcp/asset/e5912890-f78a-4770-bf45-aaa8055c54e1';
	const helloBadgeDeco = 'https://www.figma.com/api/mcp/asset/6ab31ccb-05e4-4104-a844-85aa2343c5a7';

	const words = ['Hello!', '你好!', 'สวัสดี!'];
	let wordIndex = $state(0);

	onMount(() => {
		const id = setInterval(() => {
			wordIndex = (wordIndex + 1) % words.length;
		}, 2500);
		return () => clearInterval(id);
	});
</script>

<section
	id="home"
	class="relative flex min-h-[846px] w-full items-end justify-center overflow-hidden pb-16"
>
	<!-- Orange ellipse background -->
	<div
		class="pointer-events-none absolute bottom-0 left-1/2 h-[406px] w-[812px] -translate-x-1/2 select-none"
	>
		<img src={ellipseOrange} alt="" class="h-full w-full object-cover" />
	</div>

	<!-- Heading text (behind photo, lower z) -->
	<div class="absolute top-[37px] left-1/2 z-0 flex -translate-x-1/2 flex-col items-center gap-2.5">
		<!-- Hello badge -->
		<div class="relative flex items-start">
			<div
				class="mt-5 flex w-[180px] items-center justify-center overflow-hidden rounded-[38px] border border-[#171717] bg-white/10 py-[13px]"
			>
				{#key wordIndex}
					<p class="hello-text font-lufga text-xl leading-normal tracking-[-0.3px] text-[#171717]">
						{words[wordIndex]}
					</p>
				{/key}
			</div>
			<div class="pointer-events-none relative mt-0 ml-[-14px] h-[28px] w-[27px] select-none">
				<img src={helloBadgeDeco} alt="" class="h-full w-full object-contain" />
			</div>
		</div>

		<!-- Main heading -->
		<h1
			class="w-[913px] text-center font-vast text-[95px] leading-none tracking-[-1.43px] text-[#171717]"
		>
			I'm <span class="text-[#fd853a]">Yao SiYi</span>,<br />Chinese Teacher
		</h1>
	</div>
	<!-- Woman photo (in front of text) -->
	<div class="relative z-10 mx-auto h-[636px] w-[952px] flex-shrink-0">
		<img
			src={womanPhoto}
			alt="Yao SiYi, Product Designer"
			class="h-full w-full object-contain object-bottom"
		/>
	</div>

	<!-- Bottom CTA pills (in front of photo) -->
	<div
		class="absolute bottom-[43px] left-1/2 z-20 flex h-[82px] w-[367px] -translate-x-1/2 items-center justify-center gap-2.5 rounded-[50px] bg-white/10 px-2.5"
	>
		<a
			href="#portfolio"
			class="flex w-[208px] items-center justify-center gap-0 rounded-[60px] border border-[#d0d5dd]/50 bg-[#fd853a] px-5 py-2.5 transition-all hover:brightness-110"
		>
			<span
				class="font-lufga text-[25px] leading-normal font-medium tracking-[-0.39px] whitespace-nowrap text-white"
				>Portfolio</span
			>
			<div class="relative size-[42px] flex-shrink-0 overflow-hidden">
				<div class="absolute inset-[29%]">
					<div class="absolute inset-[-6%]">
						<img src={arrowIcon} alt="" class="h-full w-full object-contain" />
					</div>
				</div>
				<div class="absolute inset-[29%]">
					<div class="absolute inset-[-6%]">
						<img src={arrowIcon2} alt="" class="h-full w-full object-contain" />
					</div>
				</div>
			</div>
		</a>
		<a
			href="#contact"
			class="flex flex-1 items-center justify-center rounded-[70px] px-2.5 py-2.5 transition-colors hover:bg-white/10"
		>
			<span
				class="font-lufga text-[25px] leading-normal font-light tracking-[-0.39px] whitespace-nowrap text-white"
				>Hire me</span
			>
		</a>
	</div>
</section>

<style>
	@keyframes fadeUp {
		from {
			opacity: 0;
			transform: translateY(8px);
		}
		to {
			opacity: 1;
			transform: translateY(0);
		}
	}

	.hello-text {
		animation: fadeUp 0.4s ease forwards;
	}
</style>
