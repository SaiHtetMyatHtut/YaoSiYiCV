<script lang="ts">
  const quoteIcon = 'https://www.figma.com/api/mcp/asset/7f6c6041-1b1d-46c2-9c25-5a555f532248';
  const starIcon = 'https://www.figma.com/api/mcp/asset/eb0296c5-33d2-40d0-88ce-afd0007be31d';
  const bgTexture = 'https://www.figma.com/api/mcp/asset/2949133e-35eb-48f0-a7f3-11f3d4b8b972';
  const blobDecor = 'https://www.figma.com/api/mcp/asset/16a9bfd6-9c6c-4bc6-be54-2067feb22568';

  const testimonials = [
    {
      name: 'Sarah Johnson',
      role: 'CEO, TechStart',
      text: "Working with Yao SiYi was an absolute pleasure. Her design skills are exceptional, and she delivered exactly what we envisioned for our product. Highly recommended!",
      rating: 5,
    },
    {
      name: 'Michael Chen',
      role: 'Founder, AppVenture',
      text: "Yao SiYi's attention to detail and user-centered approach transformed our app's UX completely. Our conversion rates improved by 40% after her redesign.",
      rating: 5,
    },
    {
      name: 'Priya Sharma',
      role: 'Product Manager, FinTech Co.',
      text: "Exceptional work! Jenny not only delivered beautiful designs but also provided strategic insights that elevated our entire product experience.",
      rating: 5,
    },
  ];
</script>

<section class="relative w-full rounded-[50px] overflow-hidden bg-[#171717] px-[71px] py-[116px] flex flex-col gap-16 items-center">
  <!-- Background texture -->
  <div class="absolute inset-0 pointer-events-none select-none">
    <img src={bgTexture} alt="" class="w-full h-full object-cover opacity-20" />
  </div>
  <!-- Blob decoration -->
  <div class="absolute right-[-100px] top-[50px] w-[600px] h-[600px] opacity-30 pointer-events-none select-none">
    <img src={blobDecor} alt="" class="w-full h-full object-contain" />
  </div>

  <!-- Heading -->
  <div class="relative z-10 text-center">
    <h2 class="font-vast text-[#fcfcfd] text-[48px] tracking-[-0.72px] leading-tight">
      Testimonials That <span class="text-[#fd853a]">Speak to</span><br />My Results
    </h2>
  </div>

  <!-- Cards row -->
  <div class="relative z-10 flex items-start gap-6 w-full max-w-[1299px]">
    {#each testimonials as t}
      <div class="flex flex-col gap-6 bg-white/5 border border-white/10 rounded-[35px] p-10 flex-1">
        <!-- Quote icon -->
        <div class="size-9 flex-shrink-0">
          <img src={quoteIcon} alt="" class="size-full" />
        </div>

        <!-- Testimonial text -->
        <p class="font-lufga text-white/80 text-xl tracking-[-0.3px] leading-relaxed flex-1">
          "{t.text}"
        </p>

        <!-- Stars -->
        <div class="flex items-center gap-1">
          {#each Array(t.rating) as _}
            <div class="size-6">
              <img src={starIcon} alt="" class="size-full" />
            </div>
          {/each}
        </div>

        <!-- Author -->
        <div class="flex items-center gap-4">
          <div class="size-12 rounded-full bg-[#fd853a]/20 flex items-center justify-center flex-shrink-0">
            <span class="font-lufga font-bold text-[#fd853a] text-xl">{t.name[0]}</span>
          </div>
          <div>
            <p class="font-lufga font-semibold text-white text-lg leading-none">{t.name}</p>
            <p class="font-lufga text-white/50 text-base mt-1">{t.role}</p>
          </div>
        </div>
      </div>
    {/each}
  </div>

  <!-- Navigation dots -->
  <div class="relative z-10 flex items-center gap-[11px]">
    <div class="bg-[#fd853a] h-[15px] rounded-full w-[60px]"></div>
    <div class="bg-white/20 rounded-full size-[15px]"></div>
    <div class="bg-white/20 rounded-full size-[15px]"></div>
  </div>
</section>
