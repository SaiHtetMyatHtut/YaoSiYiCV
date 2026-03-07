<script lang="ts">
  const timelineLine = 'https://www.figma.com/api/mcp/asset/ad1d8896-ffa8-4dda-8001-fac10e421d2f';
  const circleOrange = 'https://www.figma.com/api/mcp/asset/49b99e4b-31f6-475f-a0b2-583aab16e2dd';
  const circleDark = 'https://www.figma.com/api/mcp/asset/5f355701-3f9c-491a-b9be-eb2affbfc329';

  const experiences = [
    {
      company: 'Cognizant, Mumbai',
      period: 'Sep 2016- July 2020',
      role: 'Experince Designer',
      description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis lacus nunc, posuere in justo vulputate, bibendum sodales',
      circleImg: circleOrange,
    },
    {
      company: 'Sugee Pvt limited, Mumbai',
      period: 'Sep 2020- July 2023',
      role: 'UI/UX Designer',
      description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis lacus nunc, posuere in justo vulputate, bibendum sodales',
      circleImg: circleDark,
    },
    {
      company: 'Cinetstox, Mumbai',
      period: 'Sep 2023',
      role: 'Lead UX Designer',
      description: null,
      circleImg: circleOrange,
    },
  ];
</script>

<section id="resume" class="w-full px-[71px] flex flex-col items-center">
  <!-- Heading -->
  <div class="flex items-center justify-center py-[85px] w-full">
    <h2 class="font-vast text-[#344054] text-[64px] tracking-[-0.96px] leading-none whitespace-nowrap">
      My <span class="text-[#fd853a]">Work Experince</span>
    </h2>
  </div>

  <!-- Timeline row -->
  <div class="flex items-start justify-between w-full max-w-[1298px] pb-[155px]">
    <!-- Left: Company names -->
    <div class="flex flex-col gap-[102px] items-start">
      {#each experiences as exp}
        <div class="flex flex-col gap-[14px] items-start">
          <p class="font-lufga font-semibold text-[#344054] text-[40px] tracking-[-0.6px] leading-none whitespace-nowrap">
            {exp.company}
          </p>
          <p class="font-lufga text-[#98a2b3] text-[24px] tracking-[-0.36px] leading-none whitespace-nowrap">
            {exp.period}
          </p>
        </div>
      {/each}
    </div>

    <!-- Center: Timeline -->
    <div class="relative flex gap-2.5 h-[400px] items-start">
      <!-- Vertical dashed line -->
      <div class="absolute left-1/2 -translate-x-1/2 flex items-center justify-center h-[394px] w-0 top-0">
        <div class="rotate-90 flex-none">
          <div class="relative h-0 w-[394px]">
            <div class="absolute -top-[3px] inset-x-0">
              <img src={timelineLine} alt="" class="w-full" />
            </div>
          </div>
        </div>
      </div>

      <!-- Circles -->
      <div class="flex flex-col justify-between h-full items-start">
        {#each experiences as exp}
          <div class="relative size-[48px]">
            <div class="absolute inset-[-2%]">
              <img src={exp.circleImg} alt="" class="w-full h-full object-contain" />
            </div>
          </div>
        {/each}
      </div>
    </div>

    <!-- Right: Roles + descriptions -->
    <div class="flex flex-col gap-12 items-start">
      {#each experiences as exp}
        <div class="flex flex-col gap-[14px] items-start">
          <p class="font-lufga font-semibold text-[#344054] text-[40px] tracking-[-0.6px] leading-none whitespace-nowrap">
            {exp.role}
          </p>
          {#if exp.description}
            <p class="font-lufga font-medium text-[#98a2b3] text-[20px] tracking-[-0.3px] leading-normal w-[444px]">
              {exp.description}
            </p>
          {/if}
        </div>
      {/each}
    </div>
  </div>
</section>
