<script lang="ts">
  import Navbar from '$lib/components/Navbar.svelte';
  import Hero from '$lib/components/Hero.svelte';
  import Services from '$lib/components/Services.svelte';
  import WorkExperience from '$lib/components/WorkExperience.svelte';
  import WhyHireMe from '$lib/components/WhyHireMe.svelte';
  import Portfolio from '$lib/components/Portfolio.svelte';
  import Testimonials from '$lib/components/Testimonials.svelte';
  import CTASection from '$lib/components/CTASection.svelte';
  import BlogSection from '$lib/components/BlogSection.svelte';
  import Footer from '$lib/components/Footer.svelte';
</script>

<div class="min-w-[1440px]">
  <Navbar />

  <main>
    <!-- Hero Section -->
    <Hero />

    <!-- Services Section -->
    <div class="px-4 mt-[-40px]">
      <Services />
    </div>

    <!-- Work Experience Section -->
    <WorkExperience />

    <!-- Why Hire Me Section -->
    <WhyHireMe />

    <!-- Portfolio Section -->
    <Portfolio />

    <!-- Testimonials Section -->
    <div class="px-4 mb-0">
      <Testimonials />
    </div>

    <!-- CTA Section -->
    <CTASection />

    <!-- Blog Section -->
    <BlogSection />
  </main>

  <!-- Footer -->
  <Footer />
</div>
