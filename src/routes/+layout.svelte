<script>
  import "../app.css";
  import DrawerIcon from "$lib/components/DrawerIcon.svelte";
  import FeelDx from "$lib/static/FeelDX.svelte";

  let { data, children } = $props();
  const { menu } = data;
</script>

<div>
  <div class="drawer drawer-end">
    <input id="my-drawer-3" type="checkbox" class="drawer-toggle" />
    <div class="drawer-content flex flex-col">
      <!-- Navbar -->
      <div class="navbar bg-white w-full p-4">
        <div class="mx-2 flex-1 px-2">
          <a href="/">
            <FeelDx />
          </a>
        </div>
        <div class="hidden flex-none lg:block">
          <ul class="menu menu-horizontal">
            <!-- Navbar menu content here -->
            {#if menu}
              {#each menu as item}
                <li>
                  <a class="font-semibold tracking-wide" href={item.url}>
                    {item.text}
                  </a>
                </li>
              {/each}
            {/if}
          </ul>
        </div>
        <DrawerIcon />
      </div>
      <!-- Page content here -->
      <div>
        {@render children()}
      </div>
    </div>
    <div class="drawer-side">
      <label for="my-drawer-3" aria-label="close sidebar" class="drawer-overlay"
      ></label>
      <ul class="menu bg-base-200 min-h-full w-80 p-4">
        <!-- Sidebar content here -->
        {#if menu}
          {#each menu as item}
            <li class="py-2">
              <a class="text-xl font-bold tracking-wide" href={item.url}>
                {item.text}
              </a>
            </li>
          {/each}
        {/if}
      </ul>
    </div>
  </div>
</div>
