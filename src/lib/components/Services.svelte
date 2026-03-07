<script lang="ts">
  const bgTexture = 'https://www.figma.com/api/mcp/asset/2949133e-35eb-48f0-a7f3-11f3d4b8b972';
  const blobDecor = 'https://www.figma.com/api/mcp/asset/16a9bfd6-9c6c-4bc6-be54-2067feb22568';
  const cardMask = 'https://www.figma.com/api/mcp/asset/efe57c87-09d1-4c6e-a3f6-36adc2f91c11';
  const cardBgGlass = 'https://www.figma.com/api/mcp/asset/cce64495-9d29-47f7-bc75-404c744cc491';
  const serviceImg1 = 'https://www.figma.com/api/mcp/asset/97efa920-6b2d-458c-91e1-25ef71cac9ac';
  const serviceImg2 = 'https://www.figma.com/api/mcp/asset/72b6748a-734a-4957-8b6f-215acbc16481';
  const lineDivider = 'https://www.figma.com/api/mcp/asset/fd8400b5-89ce-4651-9aa4-2b274c013a88';
  const arrowBtnIcon = 'https://www.figma.com/api/mcp/asset/b0779823-6c38-48c0-a0e0-72a9d0ec6e7e';
  const arrowBtnIcon2 = 'https://www.figma.com/api/mcp/asset/c176969d-ad9e-4025-af57-0b2a7d274794';

  const services = [
    { title: 'UI/ UX Design', img: serviceImg1 },
    { title: 'Web Design', img: serviceImg2 },
    { title: 'Landing Page', img: serviceImg1 },
  ];
</script>

<section id="services" class="relative w-full rounded-[50px] overflow-hidden bg-[#171717] px-[71px] py-[116px] flex flex-col gap-24 items-center">
  <!-- Background texture -->
  <div class="absolute inset-0 pointer-events-none select-none">
    <img src={bgTexture} alt="" class="w-full h-full object-cover opacity-20" />
  </div>

  <!-- Blob decorations -->
  <div class="absolute right-[0px] top-[146px] w-[873px] h-[873px] pointer-events-none select-none opacity-60">
    <img src={blobDecor} alt="" class="w-full h-full object-cover" />
  </div>
  <div class="absolute left-[-184px] top-0 w-[590px] h-[594px] pointer-events-none select-none opacity-40 blur-[1.5px] rotate-[151deg]">
    <img src={blobDecor} alt="" class="w-full h-full object-cover" />
  </div>

  <!-- Header row -->
  <div class="relative flex items-end justify-between w-full max-w-[1299px] z-10">
    <h2 class="font-vast text-[#fcfcfd] text-[48px] tracking-[-0.72px] leading-none whitespace-nowrap">
      My <span class="text-[#fd853a]">Services</span>
    </h2>
    <p class="font-lufga text-white/80 text-xl tracking-[-0.3px] leading-normal w-[576px]">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis lacus nunc, posuere in justo vulputate, bibendum sodales
    </p>
  </div>

  <!-- Service cards -->
  <div class="relative flex flex-col items-center gap-10 z-10">
    <div class="flex items-start justify-between gap-4 w-full max-w-[1299px]">
      {#each services as service}
        <div class="relative w-[416px] h-[508px] flex-shrink-0">
          <!-- Card glass border -->
          <div
            class="absolute inset-0 w-[416px] h-[508px]"
            style="mask-image: url('{cardMask}'); mask-size: 416px 508px; mask-position: 0 0; mask-repeat: no-repeat;"
          >
            <img src={cardBgGlass} alt="" class="absolute inset-0 w-full h-full object-cover" />
          </div>

          <!-- Card image area -->
          <div
            class="absolute left-0 top-[158px] w-[416px] pb-[307px] flex flex-col items-center"
            style="mask-image: url('{cardMask}'); mask-size: 416px 508px; mask-position: 0px -158px; mask-repeat: no-repeat;"
          >
            <div class="bg-[#757575] h-[329px] -mb-[307px] opacity-50 rounded-[35px] w-[328px] shrink-0"></div>
            <div class="bg-[#9e9d9d] h-[329px] -mb-[307px] rounded-[35px] w-[374px] shrink-0"></div>
            <div class="h-[307px] -mb-[307px] relative rounded-[35px] w-[416px] shrink-0 overflow-hidden">
              <img src={service.img} alt={service.title} class="absolute inset-0 w-full h-full object-cover rounded-[35px]" />
            </div>
          </div>

          <!-- Card title + line -->
          <div
            class="absolute left-0 top-[44px] w-[416px] flex flex-col gap-[23px] items-start"
            style="mask-image: url('{cardMask}'); mask-size: 416px 508px; mask-position: 0px -44px; mask-repeat: no-repeat;"
          >
            <div class="flex items-start px-[37px] w-full">
              <p class="font-lufga font-medium text-white text-[32px] tracking-[-0.48px] leading-normal">{service.title}</p>
            </div>
            <div class="relative w-[416px] h-0">
              <div class="absolute -top-0.5 inset-x-0">
                <img src={lineDivider} alt="" class="w-full" />
              </div>
            </div>
          </div>

          <!-- Arrow button -->
          <div class="absolute left-[302px] top-[394px] size-[114px] flex items-center justify-center -rotate-90">
            <button class="bg-[#1d2939] flex items-center justify-center p-[21px] rounded-full size-[114px] hover:bg-[#fd853a] transition-colors group">
              <div class="size-full overflow-hidden relative rotate-90">
                <div class="absolute inset-[29%]">
                  <div class="absolute inset-[-7%]">
                    <img src={arrowBtnIcon} alt="" class="w-full h-full object-contain" />
                  </div>
                </div>
                <div class="absolute inset-[29%]">
                  <div class="absolute inset-[-7%]">
                    <img src={arrowBtnIcon2} alt="" class="w-full h-full object-contain" />
                  </div>
                </div>
              </div>
            </button>
          </div>
        </div>
      {/each}
    </div>

    <!-- Carousel dots -->
    <div class="flex items-center gap-[11px]">
      <div class="bg-[#fd853a] h-[15px] rounded-full w-[60px]"></div>
      <div class="bg-[#e4e7ec] rounded-full size-[15px]"></div>
      <div class="bg-[#e4e7ec] rounded-full size-[15px]"></div>
      <div class="bg-[#e4e7ec] rounded-full size-[15px]"></div>
    </div>
  </div>
</section>
