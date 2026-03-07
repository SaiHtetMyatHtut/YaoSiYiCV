<script lang="ts">
  let activeTab = $state('Landing Page');

  const tabs = ['Landing Page', 'Product Design', 'Dashboard', 'Wireframe', 'User Research'];

  const arrowIcon = 'https://www.figma.com/api/mcp/asset/6983c991-f0b3-42d3-93f7-d0035c31263f';
  const arrowIcon2 = 'https://www.figma.com/api/mcp/asset/e5912890-f78a-4770-bf45-aaa8055c54e1';

  // Placeholder project images (using colored gradients in CSS)
  const projectImg1 = 'https://www.figma.com/api/mcp/asset/97efa920-6b2d-458c-91e1-25ef71cac9ac';
  const projectImg2 = 'https://www.figma.com/api/mcp/asset/72b6748a-734a-4957-8b6f-215acbc16481';
</script>

<section id="portfolio" class="w-full px-[71px] py-[97px]">
  <!-- Header row -->
  <div class="flex items-start justify-between w-full max-w-[1298px] mx-auto mb-[198px]">
    <h2 class="font-vast text-[#344054] text-[56px] tracking-[-0.84px] leading-tight w-[600px]">
      Lets have a look at my <span class="text-[#fd853a]">Portfolio</span>
    </h2>
    <a href="#" class="bg-[#fd853a] flex items-center justify-center gap-0 px-5 py-2.5 rounded-[60px] self-start mt-2 hover:brightness-110 transition-all">
      <span class="font-lufga text-white text-xl tracking-[-0.3px] leading-normal whitespace-nowrap font-medium">See All</span>
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
  </div>

  <div class="flex flex-col items-center gap-0 max-w-[1290px] mx-auto">
    <!-- Portfolio cards row -->
    <div class="flex gap-[24px] w-full mb-[15px]">
      <div class="relative w-[633px] h-[371px] rounded-[35px] overflow-hidden flex-shrink-0">
        <img src={projectImg2} alt="Lirante Food Delivery" class="w-full h-full object-cover" />
      </div>
      <div class="relative w-[633px] h-[371px] rounded-[35px] overflow-hidden flex-shrink-0">
        <img src={projectImg1} alt="Portfolio project" class="w-full h-full object-cover" />
      </div>
    </div>

    <!-- Carousel dots -->
    <div class="flex items-center gap-[11px] mb-[67px] self-center">
      <div class="bg-[#fd853a] h-[15px] rounded-full w-[60px]"></div>
      <div class="bg-[#e4e7ec] rounded-full size-[15px]"></div>
      <div class="bg-[#e4e7ec] rounded-full size-[15px]"></div>
      <div class="bg-[#e4e7ec] rounded-full size-[15px]"></div>
    </div>

    <!-- Category tabs -->
    <div class="flex items-center gap-4 mb-[102px]">
      {#each tabs as tab}
        <button
          onclick={() => activeTab = tab}
          class="px-6 py-3 rounded-full text-xl tracking-[-0.3px] leading-normal font-lufga transition-all {activeTab === tab ? 'bg-[#fd853a] text-white font-medium' : 'bg-[#f2f4f7] text-[#344054] hover:bg-[#e4e7ec]'}"
        >
          {tab}
        </button>
      {/each}
    </div>

    <!-- Project info -->
    <div class="flex flex-col gap-[24px] w-[742px] self-start ml-[274px]">
      <div class="flex items-start justify-between w-full">
        <h3 class="font-lufga font-semibold text-[#344054] text-[52px] tracking-[-0.78px] leading-tight">
          Lirante - Food Dilvery Solution
        </h3>
        <a href="#" class="flex items-center justify-center bg-[#1d2939] rounded-full size-[58px] hover:bg-[#fd853a] transition-colors flex-shrink-0 mt-1">
          <div class="size-[26px] overflow-hidden relative">
            <div class="absolute inset-[20%]">
              <img src={arrowIcon} alt="" class="w-full h-full object-contain" />
            </div>
          </div>
        </a>
      </div>
      <p class="font-lufga text-[#98a2b3] text-xl tracking-[-0.3px] leading-normal">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed congue interdum ligula a dignissim. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed lobortis orci elementum egestas lobortis.
      </p>
    </div>
  </div>
</section>
