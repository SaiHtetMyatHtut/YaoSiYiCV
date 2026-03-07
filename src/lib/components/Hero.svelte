<script lang="ts">
  const womanPhoto = 'https://www.figma.com/api/mcp/asset/73a2d19a-e55c-4c4d-8bed-d9a520b72c60';
  const ellipseOrange = 'https://www.figma.com/api/mcp/asset/31941aae-534b-4050-88d9-0f0b4167a9e4';
  const quoteIcon = 'https://www.figma.com/api/mcp/asset/7f6c6041-1b1d-46c2-9c25-5a555f532248';
  const starIcon = 'https://www.figma.com/api/mcp/asset/eb0296c5-33d2-40d0-88ce-afd0007be31d';
  const arrowIcon = 'https://www.figma.com/api/mcp/asset/6983c991-f0b3-42d3-93f7-d0035c31263f';
  const arrowIcon2 = 'https://www.figma.com/api/mcp/asset/e5912890-f78a-4770-bf45-aaa8055c54e1';
  const helloBadgeDeco = 'https://www.figma.com/api/mcp/asset/6ab31ccb-05e4-4104-a844-85aa2343c5a7';
</script>

<section id="home" class="relative w-full min-h-[846px] flex items-end justify-center overflow-hidden pb-16">
  <!-- Orange ellipse background -->
  <div class="absolute bottom-0 left-1/2 -translate-x-1/2 w-[812px] h-[406px] pointer-events-none select-none">
    <img src={ellipseOrange} alt="" class="w-full h-full object-cover" />
  </div>

  <!-- Heading text (behind photo, lower z) -->
  <div class="absolute top-[37px] left-1/2 -translate-x-1/2 flex flex-col items-center gap-2.5 z-0">
    <!-- Hello badge -->
    <div class="relative flex items-start">
      <div class="border border-[#171717] bg-white/10 rounded-[38px] px-[25px] py-[13px] mt-5">
        <p class="font-lufga text-[#171717] text-xl tracking-[-0.3px] leading-normal whitespace-nowrap">Hello!</p>
      </div>
      <div class="w-[27px] h-[28px] ml-[-14px] mt-0 relative pointer-events-none select-none">
        <img src={helloBadgeDeco} alt="" class="w-full h-full object-contain" />
      </div>
    </div>

    <!-- Main heading -->
    <h1 class="font-vast text-[95px] text-[#171717] text-center tracking-[-1.43px] leading-none w-[913px]">
      I'm <span class="text-[#fd853a]">Yao SiYi</span>,<br />Chinese Teacher
    </h1>
  </div>

  <!-- Woman photo (in front of text) -->
  <div class="relative z-10 w-[952px] h-[636px] flex-shrink-0 mx-auto">
    <img src={womanPhoto} alt="Yao SiYi, Product Designer" class="w-full h-full object-contain object-bottom" />
  </div>

  <!-- Left testimonial quote -->
  <div class="absolute left-[71px] top-[373px] flex flex-col gap-6 z-20">
    <div class="size-9">
      <img src={quoteIcon} alt="" class="size-full" />
    </div>
    <p class="font-lufga text-[#344054] text-xl tracking-[-0.3px] leading-normal">
      Yao SiYi's Exceptional product design<br />
      ensure our website's success.<br />
      Highly Recommended
    </p>
  </div>

  <!-- Right stars + experience -->
  <div class="absolute right-[71px] top-[380px] flex flex-col gap-5 items-end z-20">
    <div class="flex items-center">
      {#each Array(5) as _}
        <div class="size-8">
          <img src={starIcon} alt="" class="size-full" />
        </div>
      {/each}
    </div>
    <div class="flex flex-col items-center gap-1 text-[#171717] text-center">
      <p class="font-urbanist font-bold text-[47px] tracking-[-0.71px] leading-none">10 Years</p>
      <p class="font-lufga text-xl tracking-[-0.3px] leading-normal">Experince</p>
    </div>
  </div>

  <!-- Bottom CTA pills (in front of photo) -->
  <div class="absolute bottom-[43px] left-1/2 -translate-x-1/2 bg-white/10 flex gap-2.5 items-center justify-center h-[82px] px-2.5 rounded-[50px] w-[367px] z-20">
    <a href="#portfolio" class="bg-[#fd853a] border border-[#d0d5dd]/50 flex items-center justify-center gap-0 px-5 py-2.5 rounded-[60px] w-[208px] hover:brightness-110 transition-all">
      <span class="font-lufga text-white text-[25px] tracking-[-0.39px] leading-normal whitespace-nowrap font-medium">Portfolio</span>
      <div class="size-[42px] overflow-hidden relative flex-shrink-0">
        <div class="absolute inset-[29%]">
          <div class="absolute inset-[-6%]">
            <img src={arrowIcon} alt="" class="w-full h-full object-contain" />
          </div>
        </div>
        <div class="absolute inset-[29%]">
          <div class="absolute inset-[-6%]">
            <img src={arrowIcon2} alt="" class="w-full h-full object-contain" />
          </div>
        </div>
      </div>
    </a>
    <a href="#contact" class="flex flex-1 items-center justify-center px-5 py-2.5 rounded-[60px] hover:bg-white/10 transition-colors">
      <span class="font-lufga text-white text-[25px] tracking-[-0.39px] leading-normal whitespace-nowrap font-light">Hire me</span>
    </a>
  </div>
</section>
