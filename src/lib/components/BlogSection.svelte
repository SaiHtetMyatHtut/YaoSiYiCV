<script lang="ts">
  const arrowIcon = 'https://www.figma.com/api/mcp/asset/6983c991-f0b3-42d3-93f7-d0035c31263f';
  const arrowIcon2 = 'https://www.figma.com/api/mcp/asset/e5912890-f78a-4770-bf45-aaa8055c54e1';

  const posts = [
    {
      category: 'UX Design',
      title: 'Design Unleashed: Behind The Scenes of UX Ninja Ninja',
      date: 'March 15, 2024',
      bgClass: 'from-[#4f46e5] to-[#7c3aed]',
      brand: 'UX NINJA',
    },
    {
      category: 'App Design',
      title: 'Sugee: Leave Management System for the Auto Sector',
      date: 'February 28, 2024',
      bgClass: 'from-[#7c3aed] to-[#1e1b4b]',
      brand: 'sugee',
    },
    {
      category: 'Dashboard',
      title: 'Controlhub Navigation: How to Invest in Digital Media',
      date: 'January 20, 2024',
      bgClass: 'from-[#1e293b] to-[#0f172a]',
      brand: 'Controlhub',
    },
  ];
</script>

<section class="w-full px-[71px] py-[97px]">
  <!-- Header row -->
  <div class="flex items-start justify-between w-full max-w-[1298px] mx-auto mb-[174px]">
    <h2 class="font-vast text-[#344054] text-[56px] tracking-[-0.84px] leading-tight w-[350px]">
      From my <span class="text-[#fd853a]">blog post</span>
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

  <!-- Blog cards grid -->
  <div class="grid grid-cols-3 gap-[25px] w-full max-w-[1299px] mx-auto">
    {#each posts as post}
      <article class="flex flex-col rounded-[35px] overflow-hidden border border-[#e4e7ec] hover:shadow-xl transition-shadow cursor-pointer">
        <!-- Card image area -->
        <div class="h-[380px] bg-gradient-to-br {post.bgClass} relative overflow-hidden flex items-center justify-center">
          <span class="font-urbanist font-bold text-white/30 text-[48px] tracking-tight select-none">{post.brand}</span>
        </div>

        <!-- Card content -->
        <div class="flex flex-col gap-4 p-8 flex-1">
          <div class="flex items-center justify-between">
            <span class="font-lufga text-[#fd853a] text-base tracking-[-0.24px] font-medium">{post.category}</span>
            <span class="font-lufga text-[#98a2b3] text-sm">{post.date}</span>
          </div>
          <h3 class="font-lufga font-semibold text-[#344054] text-[22px] tracking-[-0.33px] leading-snug">
            {post.title}
          </h3>
          <a href="#" class="flex items-center gap-2 text-[#fd853a] font-lufga font-medium text-lg mt-auto hover:gap-3 transition-all">
            Read more
            <svg class="size-5" viewBox="0 0 20 20" fill="none">
              <path d="M4 10h12M12 6l4 4-4 4" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
            </svg>
          </a>
        </div>
      </article>
    {/each}
  </div>
</section>
