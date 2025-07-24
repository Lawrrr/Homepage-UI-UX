<script>
  import Services from "$lib/components/Services.svelte";
  import Testimonials from "$lib/components/Testimonials.svelte";

  const { data } = $props();
  const { testimonials } = data;
</script>

<div class="container mx-auto">
  <Services />
  <Testimonials {testimonials} />
</div>
