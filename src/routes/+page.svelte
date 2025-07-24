<script>
  import Testimonials from "$lib/components/Testimonials.svelte";

  const { data } = $props();
  const { testimonials } = data;
</script>

<div class="container mx-auto">
  <Testimonials {testimonials} />
</div>
