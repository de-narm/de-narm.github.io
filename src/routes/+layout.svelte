<script lang="ts">
	import './layout.css';
	import logo from '$lib/assets/logo.svg';
	import github from '$lib/assets/github.svg';
	import { page } from '$app/state';

	let { children } = $props();

  let scrollContainerHeight: number = $state();
</script>

<svelte:head>
  <link rel="icon" href={logo} />
</svelte:head>

{#snippet navButton(text: string, target:string)}
  {@const isOpen = page.url.pathname == target}
  <div class="px-3 py-1 rounded-md
              {isOpen ? 'bg-zinc-800 text-white' : 'text-zinc-400'}">
    <a href={target}>{text}</a>
  </div>
{/snippet}

{#snippet footerButton(text: string, target:string)}
  <span>
    <a href={target}>{text}</a>
  </span>
{/snippet}

<div class="w-screen h-screen overflow-hidden bg-black/93 text-white
            flex flex-col">
  <!-- Navigation -->
  <div class="w-full h-fit flex justify-center">
    <div class="max-w-[980px] w-5/6 p-5 z-1">
      <nav class="flex justify-between my-5">
        <div class="flex gap-1 items-center">
          <img class="w-[30px]" src={logo}>
          <span class="font-extrabold pl-1 pr-3 text-2xl">Explorama</span>
          {@render navButton("Home", "/")}
        </div>
        <a href="https://github.com/Explorama/Explorama">
          <img class="w-[30px] opacity-70" src="{github}">
        </a>
      </nav>
    </div>
  </div>
  
  <!-- Main Container -->
  <div class="w-full h-full flex relative items-center 
              overflow-y-auto flex-col">
    <!-- Page -->
    <div bind:clientHeight={scrollContainerHeight} 
         class="max-w-[980px] w-5/6 p-5 z-1">
      {@render children()}
    </div>
    
    <!-- Footer -->
    <div class="w-full z-1 flex justify-center text-white/80">
      <div class="bg-black/95 max-w-[980px] w-5/6 p-10 z-1 flex rounded-t-md">
        <div class="w-full flex flex-col">
          <span class="text-zinc-500 mb-1">Follow us</span> 
          {@render footerButton("Github", 
                                "https://github.com/Explorama/Explorama")}
        </div>
        <div class="w-full flex flex-col">
          <span class="text-zinc-500 mb-1">Learn</span> 
          {@render footerButton("About", 
                                "/about")}
        </div>
        <div class="w-full flex flex-col">
          <span class="text-zinc-500 mb-1">Impressum</span> 
          <span>Explorama e.V.</span>
          <span>Ernst-Horn-Straße 28g</span>
          <span>22525 Hamburg</span>
        </div>
      </div>
    </div>

    <!-- Grid Container -->
    <div class="absolute z-0 top-0 w-full
                max-w-[1180px] opacity-80"
         style="height: {scrollContainerHeight ?? 0}px;">
      <div class="absolute inset-0 h-full w-full flex
                  mask-y-from-95% mask-x-from-80% overflow-hidden">
        <div class="absolute top-[31px] left-[31px] h-full w-full
                    bg-[radial-gradient(circle,#232525ff_5px,transparent_5px)]
                    bg-[size:60px_60px]" />
        <div class="absolute h-full w-full
                    bg-[linear-gradient(to_right,#232525ff_2px,transparent_2px),linear-gradient(to_bottom,#232525ff_2px,transparent_2px)]
                    bg-[size:60px_60px]" />
      </div>
    </div>
  </div>

</div>

