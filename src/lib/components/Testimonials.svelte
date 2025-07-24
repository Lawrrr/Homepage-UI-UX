<script>
  import { Splide, SplideSlide } from "@splidejs/svelte-splide";

  const { testimonials } = $props();
  const splideOptions = {
    rewind: true,
    autoplay: true,
    gap: "1rem",
  };
</script>

<div class="md:flex py-4 px-2">
  <div class="px-8 md:py-4 md:bg-[#dfdfdf]">
    <h1
      class="text-[24px] font-semibold text-[#2A2F1E] uppercase tracking-wide"
    >
      Testimonials
    </h1>
  </div>
  <div class="flex-grow">
    <Splide options={splideOptions} aria-label="My Favorite Images">
      {#each testimonials as testimonial}
        <SplideSlide class="content-center text-center">
          <div class="m-8">
            <div>
              <p>{testimonial.content}</p>
            </div>
            <div class="pt-10">
              <p class="font-semibold text-xl">{testimonial.position}</p>
            </div>
            <div class="pt-2">
              <p>{testimonial.company}</p>
            </div>
          </div>
        </SplideSlide>
      {/each}
    </Splide>
  </div>
</div>
