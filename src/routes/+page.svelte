<script>
  import Services from "$lib/components/Services.svelte";
  import Testimonials from "$lib/components/Testimonials.svelte";
  import HeroSection from "$lib/components/HeroSection.svelte";

  const { data } = $props();
  const { testimonials } = data;
</script>

<div>
  <HeroSection />
  <div class="container mx-auto">
    <Services />
    <Testimonials {testimonials} />
  </div>
</div>
