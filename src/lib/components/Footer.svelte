<script lang="ts">
  const logoIcon = 'https://www.figma.com/api/mcp/asset/7daf4194-39d3-4a9a-92e5-f7d94e5a35b7';
  const logoText = 'https://www.figma.com/api/mcp/asset/03205008-e7d2-47ee-b9aa-23b056ea0c2e';
  const bgTexture = 'https://www.figma.com/api/mcp/asset/2949133e-35eb-48f0-a7f3-11f3d4b8b972';
  const arrowIcon = 'https://www.figma.com/api/mcp/asset/6983c991-f0b3-42d3-93f7-d0035c31263f';
  const arrowIcon2 = 'https://www.figma.com/api/mcp/asset/e5912890-f78a-4770-bf45-aaa8055c54e1';

  let newsletterEmail = $state('');

  const navLinks = ['Home', 'About Us', 'Service', 'Resume', 'Project'];
  const contactInfo = ['+91 7738443636', 'Jaycrea36@gmail.com', 'Portfolio-jcrea.com'];
</script>

<footer class="relative w-full rounded-t-[50px] overflow-hidden bg-[#171717] px-[71px] pt-[25px] pb-0">
  <!-- Background texture -->
  <div class="absolute inset-0 pointer-events-none select-none">
    <img src={bgTexture} alt="" class="w-full h-full object-cover opacity-20" />
  </div>

  <!-- Top: Lets Connect + button -->
  <div class="relative z-10 flex items-start justify-between w-full max-w-[1298px] py-[25px]">
    <h2 class="font-vast text-[#fcfcfd] text-[56px] tracking-[-0.84px] leading-tight w-[643px]">
      Lets <span class="text-[#fd853a]">Connect</span> there
    </h2>
    <a href="#contact" class="flex items-center justify-center mt-[44px] bg-white/10 border border-white/20 rounded-[50px] px-6 py-3 gap-2 hover:bg-white/20 transition-colors">
      <span class="font-lufga text-white text-xl tracking-[-0.3px] leading-normal font-medium">Hire me</span>
      <div class="size-[42px] overflow-hidden relative flex-shrink-0">
        <div class="absolute inset-[29%]">
          <div class="absolute inset-[-6%]">
            <img src={arrowIcon} alt="" class="w-full h-full object-contain opacity-70" />
          </div>
        </div>
      </div>
    </a>
  </div>

  <!-- Divider line -->
  <div class="relative z-10 w-full max-w-[1298px] h-px bg-white/10 my-0"></div>

  <!-- Main footer content -->
  <div class="relative z-10 flex items-start justify-between w-full max-w-[1298px] py-[60px] gap-8">
    <!-- Column 1: Logo + social + description -->
    <div class="flex flex-col gap-[30px] w-[635px]">
      <!-- Logo -->
      <a href="#home" class="flex gap-2.5 items-center">
        <div class="size-[46px] relative flex-shrink-0">
          <img src={logoIcon} alt="" class="size-full object-contain" />
        </div>
        <div class="h-[19px] w-[83px] relative">
          <img src={logoText} alt="JCREA" class="h-full w-auto object-contain" />
        </div>
      </a>

      <!-- Description -->
      <p class="font-lufga text-white/60 text-xl tracking-[-0.3px] leading-relaxed">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed congue interdum ligula a dignissim. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed lobortis orci elementum egestas lobortis.
      </p>

      <!-- Social icons -->
      <div class="flex items-center gap-[5px]">
        <!-- Facebook -->
        <a href="#" aria-label="Facebook" class="size-6 flex items-center justify-center hover:opacity-70 transition-opacity">
          <svg viewBox="0 0 24 24" fill="#fcfcfd" class="size-6">
            <path d="M18 2h-3a5 5 0 0 0-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 0 1 1-1h3z"/>
          </svg>
        </a>
        <!-- YouTube -->
        <a href="#" aria-label="YouTube" class="size-6 flex items-center justify-center hover:opacity-70 transition-opacity">
          <svg viewBox="0 0 24 24" fill="#fcfcfd" class="size-6">
            <path d="M22.54 6.42a2.78 2.78 0 0 0-1.95-1.96C18.88 4 12 4 12 4s-6.88 0-8.59.46a2.78 2.78 0 0 0-1.95 1.96A29 29 0 0 0 1 12a29 29 0 0 0 .46 5.58A2.78 2.78 0 0 0 3.41 19.6C5.12 20 12 20 12 20s6.88 0 8.59-.46a2.78 2.78 0 0 0 1.95-1.95A29 29 0 0 0 23 12a29 29 0 0 0-.46-5.58z"/>
            <polygon points="9.75,15.02 15.5,12 9.75,8.98 9.75,15.02" fill="#171717"/>
          </svg>
        </a>
        <!-- WhatsApp -->
        <a href="#" aria-label="WhatsApp" class="size-6 flex items-center justify-center hover:opacity-70 transition-opacity">
          <svg viewBox="0 0 24 24" fill="#fcfcfd" class="size-6">
            <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347"/>
          </svg>
        </a>
        <!-- Instagram -->
        <a href="#" aria-label="Instagram" class="size-6 flex items-center justify-center hover:opacity-70 transition-opacity">
          <svg viewBox="0 0 24 24" fill="none" stroke="#fcfcfd" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="size-6">
            <rect x="2" y="2" width="20" height="20" rx="5" ry="5"/>
            <path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"/>
            <line x1="17.5" y1="6.5" x2="17.51" y2="6.5"/>
          </svg>
        </a>
        <!-- Twitter/X -->
        <a href="#" aria-label="Twitter" class="size-6 flex items-center justify-center hover:opacity-70 transition-opacity">
          <svg viewBox="0 0 24 24" fill="#fcfcfd" class="size-6">
            <path d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-4.714-6.231-5.401 6.231H2.744l7.73-8.835L1.254 2.25H8.08l4.254 5.622L18.244 2.25zm-1.161 17.52h1.833L7.084 4.126H5.117L17.083 19.77z"/>
          </svg>
        </a>
      </div>
    </div>

    <!-- Column 2: Navigation -->
    <div class="flex flex-col gap-[54px]">
      <p class="font-lufga font-semibold text-white text-[26px] tracking-[-0.39px] leading-none">Navigation</p>
      <div class="flex flex-col gap-[41px]">
        {#each navLinks as link}
          <a href="#{link.toLowerCase().replace(' ', '-')}" class="font-lufga text-white/60 text-xl tracking-[-0.3px] leading-none hover:text-white transition-colors">
            {link}
          </a>
        {/each}
      </div>
    </div>

    <!-- Column 3: Contact -->
    <div class="flex flex-col gap-[54px]">
      <p class="font-lufga font-semibold text-white text-[26px] tracking-[-0.39px] leading-none">Contact</p>
      <div class="flex flex-col gap-[41px]">
        {#each contactInfo as info}
          <p class="font-lufga text-white/60 text-xl tracking-[-0.3px] leading-none">{info}</p>
        {/each}
      </div>
    </div>

    <!-- Column 4: Newsletter -->
    <div class="flex flex-col gap-[54px] w-[304px]">
      <p class="font-lufga font-semibold text-white text-[26px] tracking-[-0.39px] leading-none">Get the latest information</p>
      <div class="flex items-center w-full h-[51px] rounded-full overflow-hidden border border-white/20">
        <input
          bind:value={newsletterEmail}
          type="email"
          placeholder="Email Address"
          class="flex-1 bg-transparent font-lufga text-white text-xl tracking-[-0.3px] leading-normal placeholder:text-white/40 outline-none border-none px-[14px]"
        />
        <button class="size-[51px] bg-[#fd853a] flex items-center justify-center hover:brightness-110 transition-all flex-shrink-0">
          <svg viewBox="0 0 24 24" fill="none" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="size-5 rotate-45">
            <line x1="22" y1="2" x2="11" y2="13"/>
            <polygon points="22 2 15 22 11 13 2 9 22 2"/>
          </svg>
        </button>
      </div>
    </div>
  </div>

  <!-- Bottom divider -->
  <div class="relative z-10 w-full max-w-[1298px] h-px bg-white/10"></div>

  <!-- Copyright row -->
  <div class="relative z-10 flex items-center justify-between w-full max-w-[1298px] py-[26px]">
    <p class="font-lufga text-white/40 text-[26px] tracking-[-0.39px] leading-none">
      Copyright© 2024 Yao SiYi. All Rights Reserved.
    </p>
    <p class="font-lufga text-white/40 text-[26px] tracking-[-0.39px] leading-none">
      User Terms &amp; Conditions | Privacy Policy
    </p>
  </div>
</footer>
