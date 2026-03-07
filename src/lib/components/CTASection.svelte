<script lang="ts">
  const smsIcon = 'https://www.figma.com/api/mcp/asset/7f6c6041-1b1d-46c2-9c25-5a555f532248';
  const starIcon = 'https://www.figma.com/api/mcp/asset/eb0296c5-33d2-40d0-88ce-afd0007be31d';

  let email = $state('');

  function handleSubmit(e: Event) {
    e.preventDefault();
    email = '';
  }
</script>

<section id="contact" class="w-full px-[71px] py-[98px] flex flex-col items-center gap-0">
  <!-- Heading -->
  <h2 class="font-vast text-[#344054] text-[62px] tracking-[-0.93px] leading-tight text-center w-[799px] mb-[160px]">
    Have an Awsome Project <span class="text-[#fd853a]">Idea? Let's Discuss</span>
  </h2>

  <!-- Email form -->
  <div class="flex flex-col items-center gap-0 w-[832px]">
    <form onsubmit={handleSubmit} class="w-full">
      <!-- Input row -->
      <div class="flex items-center justify-between w-full h-[86px] bg-[#f9fafb] border border-[#e4e7ec] rounded-[50px] px-[14px]">
        <div class="flex items-center gap-4 flex-1">
          <!-- Email icon decoration -->
          <div class="flex items-center justify-center size-[58px] bg-[#fd853a]/10 rounded-full flex-shrink-0">
            <div class="size-8">
              <img src={smsIcon} alt="" class="size-full object-contain opacity-80" />
            </div>
          </div>
          <input
            bind:value={email}
            type="email"
            placeholder="Enter Email Address"
            class="flex-1 bg-transparent font-lufga text-[#344054] text-xl tracking-[-0.3px] leading-normal placeholder:text-[#98a2b3] outline-none border-none"
          />
        </div>
        <button
          type="submit"
          class="bg-[#fd853a] flex items-center justify-center px-8 py-4 rounded-[60px] hover:brightness-110 transition-all"
        >
          <span class="font-lufga font-bold text-white text-xl tracking-[-0.3px] leading-normal whitespace-nowrap">Send</span>
        </button>
      </div>
    </form>

    <!-- Trust badges -->
    <div class="flex items-center justify-between w-full px-[31px] mt-6">
      <div class="flex items-center gap-2">
        <div class="size-6">
          <img src={starIcon} alt="" class="size-full" />
        </div>
        <span class="font-lufga text-[#344054] text-xl tracking-[-0.3px]">4.9/5 Average Ratings</span>
      </div>

      <div class="flex items-center gap-2">
        <div class="size-6 rounded-full bg-[#fd853a] flex items-center justify-center">
          <span class="text-white text-xs font-bold">★</span>
        </div>
        <span class="font-lufga text-[#344054] text-xl tracking-[-0.3px]">25+ Winning Awards</span>
      </div>

      <div class="flex items-center gap-2">
        <div class="size-6 rounded-full bg-[#fd853a] flex items-center justify-center">
          <span class="text-white text-xs font-bold">✓</span>
        </div>
        <span class="font-lufga text-[#344054] text-xl tracking-[-0.3px]">Certified Product Designer</span>
      </div>
    </div>
  </div>
</section>
