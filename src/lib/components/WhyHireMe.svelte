<script lang="ts">
  const womanPhoto = 'https://www.figma.com/api/mcp/asset/73a2d19a-e55c-4c4d-8bed-d9a520b72c60';
  const blobDecor = 'https://www.figma.com/api/mcp/asset/16a9bfd6-9c6c-4bc6-be54-2067feb22568';
  const arrowIcon = 'https://www.figma.com/api/mcp/asset/6983c991-f0b3-42d3-93f7-d0035c31263f';
  const arrowIcon2 = 'https://www.figma.com/api/mcp/asset/e5912890-f78a-4770-bf45-aaa8055c54e1';
</script>

<section id="about" class="relative w-full overflow-hidden py-[103px] px-[71px]">
  <!-- Background blob decorations -->
  <div class="absolute right-0 top-[50px] w-[600px] h-[600px] opacity-20 pointer-events-none select-none">
    <img src={blobDecor} alt="" class="w-full h-full object-contain" />
  </div>

  <div class="flex items-center gap-0 max-w-[1299px] mx-auto">
    <!-- Left: Photo -->
    <div class="relative w-[603px] h-[600px] flex-shrink-0 overflow-hidden rounded-[50px] bg-[#f9f0e8]">
      <img src={womanPhoto} alt="Product Designer" class="w-full h-full object-cover object-top" />
    </div>

    <!-- Right: Content -->
    <div class="flex flex-col gap-0 items-start pl-[63px] w-[696px]">
      <!-- Heading -->
      <div class="w-full mb-[47px]">
        <h2 class="font-vast text-[#344054] text-[56px] tracking-[-0.84px] leading-none">
          Why <span class="text-[#fd853a]">Hire me?</span>
        </h2>
      </div>

      <!-- Description -->
      <p class="font-lufga font-medium text-[#98a2b3] text-xl tracking-[-0.3px] leading-normal w-[444px] mb-[125px]">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis lacus nunc, posuere in justo vulputate, bibendum sodales
      </p>

      <!-- Stats -->
      <div class="flex items-start w-full mb-[90px]">
        <div class="flex flex-col gap-1 items-start w-[343px]">
          <p class="font-urbanist font-bold text-[#344054] text-[47px] tracking-[-0.71px] leading-none">450+</p>
          <p class="font-lufga text-[#98a2b3] text-[26px] tracking-[-0.36px] leading-normal">Project Completed</p>
        </div>
        <div class="flex flex-col gap-1 items-start w-[343px]">
          <p class="font-urbanist font-bold text-[#344054] text-[47px] tracking-[-0.71px] leading-none">450+</p>
          <p class="font-lufga text-[#98a2b3] text-[26px] tracking-[-0.36px] leading-normal">Project Completed</p>
        </div>
      </div>

      <!-- Hire me button -->
      <a href="#contact" class="bg-white/10 flex items-center justify-center h-[82px] px-2.5 rounded-[50px] w-[233px] border border-[#171717]/10">
        <div class="bg-[#fd853a] flex items-center justify-center gap-0 px-5 py-2.5 rounded-[60px] w-full hover:brightness-110 transition-all">
          <span class="font-lufga text-white text-[25px] tracking-[-0.39px] leading-normal whitespace-nowrap font-medium">Hire me</span>
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
        </div>
      </a>
    </div>
  </div>
</section>
