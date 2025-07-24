<script>
  import FeelDXLogoTagline from "$lib/static/images/FeelDXLogoTagline.svg";
  import Facebook from "$lib/static/images/facebook.svg";
  import Instagram from "$lib/static/images/instagram.svg";
  import Linkedin from "$lib/static/images/linkedin.svg";
  import Youtube from "$lib/static/images/youtube.svg";

  const { menu } = $props();
</script>

<footer
  class="footer md:footer-center sm:footer-horizontal bg-[#202317] text-neutral-content p-10"
>
  <div class="md:place-items-center">
    <div>
      <a href="/">
        <img src={FeelDXLogoTagline} alt="tagline" />
      </a>
    </div>
    <div class="grid grid-cols-4 gap-4 mt-2">
      <div>
        <a href="https://www.facebook.com/feeldx">
          <img class="h-8 w-8" src={Facebook} alt="facebook" />
        </a>
      </div>
      <div>
        <a href="https://www.instagram.com/feeldx/">
          <img class="h-8 w-8" src={Instagram} alt="instagram" />
        </a>
      </div>
      <div>
        <a href="https://www.linkedin.com/company/feeldx">
          <img class="h-8 w-8" src={Linkedin} alt="linkedin" />
        </a>
      </div>
      <div>
        <a href="https://www.youtube.com/channel/UC9kmR0LVnaZahPLxodFdesQ">
          <img class="h-8 w-8" src={Youtube} alt="Youtube" />
        </a>
      </div>
    </div>
    <div class="my-4">
      <p>Copyright © {new Date().getFullYear()} - All right reserved</p>
    </div>
  </div>
  <div>
    {#if menu}
      {#each menu as item}
        <li class="py-2 list-none">
          <a class="text-xl font-bold tracking-wide" href={item.url}>
            {item.text}
          </a>
        </li>
      {/each}
    {/if}
  </div>
</footer>
