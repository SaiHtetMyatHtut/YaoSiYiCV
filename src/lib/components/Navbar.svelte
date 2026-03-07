<script lang="ts">
	import { onMount } from 'svelte';

	const logoIcon = 'https://www.figma.com/api/mcp/asset/7daf4194-39d3-4a9a-92e5-f7d94e5a35b7';
	const logoText = 'https://www.figma.com/api/mcp/asset/03205008-e7d2-47ee-b9aa-23b056ea0c2e';

	let hovered = $state(false);
	let navEl: HTMLElement;
	let hireMeEl: HTMLElement;
	let pillLeft = $state(0);
	let pillWidth = $state(307);
	let clipLeft = $state(0);
	let clipRight = $state(0);

	function movePillTo(el: HTMLElement) {
		const navRect = navEl.getBoundingClientRect();
		const itemRect = el.getBoundingClientRect();
		pillLeft = itemRect.left - navRect.left;
		pillWidth = itemRect.width;
	}

	onMount(() => {
		movePillTo(hireMeEl);
		const navRect = navEl.getBoundingClientRect();
		const hireMeRect = hireMeEl.getBoundingClientRect();
		const pad = 10;
		clipLeft = hireMeRect.left - navRect.left - pad;
		clipRight = navRect.right - hireMeRect.right - pad;
	});

	let navClipPath = $derived(
		hovered
			? 'inset(0 0 0 0 round 9999px)'
			: `inset(0 ${clipRight}px 0 ${clipLeft}px round 9999px)`
	);

	function handleItemEnter(e: MouseEvent) {
		movePillTo(e.currentTarget as HTMLElement);
	}

	function handleHireMeEnter(e: MouseEvent) {
		hovered = true;
		movePillTo(e.currentTarget as HTMLElement);
	}

	function handleMouseLeave() {
		hovered = false;
		movePillTo(hireMeEl);
	}
</script>

<header class="sticky top-4 z-50 flex justify-center px-4">
	<nav
		bind:this={navEl}
		onmouseleave={handleMouseLeave}
		style="clip-path: {navClipPath}; transition: clip-path 0.45s ease;"
		class="relative flex h-[86px] items-center rounded-full border border-white/20 bg-[#171717] px-2.5 backdrop-blur-[7.5px]"
	>
		<!-- Sliding orange pill -->
		<div
			class="pointer-events-none absolute inset-y-2 rounded-full bg-[#fd853a] transition-[left,width] duration-300 ease-in-out"
			style="left: {pillLeft}px; width: {pillWidth}px;"
		></div>

		<!-- Left items -->
		<div class="flex items-center {hovered ? '' : 'pointer-events-none'}">
			<a href="#about" onmouseenter={handleItemEnter} class="nav-link relative z-10 rounded-full">
				<span class="font-lufga text-xl leading-normal tracking-[-0.3px] text-white">About</span>
			</a>
			<a href="#services" onmouseenter={handleItemEnter} class="nav-link relative z-10 rounded-full">
				<span class="font-lufga text-xl leading-normal tracking-[-0.3px] text-white">Service</span>
			</a>
		</div>

		<!-- Hire Me center -->
		<a
			href="#contact"
			bind:this={hireMeEl}
			onmouseenter={handleHireMeEnter}
			class="relative z-10 mx-1 flex w-[307px] shrink-0 items-center justify-center rounded-full px-10 py-5"
		>
			<span class="font-lufga text-xl font-bold leading-normal tracking-[-0.3px] whitespace-nowrap text-white"
				>Hire Me</span
			>
		</a>

		<!-- Right items -->
		<div class="flex items-center {hovered ? '' : 'pointer-events-none'}">
			<a href="#resume" onmouseenter={handleItemEnter} class="nav-link relative z-10 rounded-full">
				<span class="font-lufga text-xl leading-normal tracking-[-0.3px] text-white">Resume</span>
			</a>
			<a href="#portfolio" onmouseenter={handleItemEnter} class="nav-link relative z-10 rounded-full">
				<span class="font-lufga text-xl leading-normal tracking-[-0.3px] text-white">Project</span>
			</a>
		</div>
	</nav>
</header>

<style>
	.nav-link {
		display: flex;
		align-items: center;
		justify-content: center;
		padding: 1.25rem 2rem;
		white-space: nowrap;
		flex-shrink: 0;
	}

</style>
