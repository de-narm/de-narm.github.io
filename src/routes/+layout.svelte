<script lang="ts">
	import './layout.css';
	import logo from '$lib/assets/logo.svg';
	import github from '$lib/assets/github.svg';

	let { children } = $props();
</script>

<svelte:head>
  <link rel="icon" href={logo} />
</svelte:head>

{#snippet navButton(text: string, isOpen: boolean)}
  <div class="px-3 py-1 rounded-md
              {isOpen ? 'bg-zinc-800 text-white' : 'text-zinc-400'}">
    {text} 
  </div>
{/snippet}

<!-- Navigation -->
<div class="bg-black/93 text-white w-screen h-fit flex justify-center">
  <div class="w-[980px] p-5 z-1">
    <nav class="flex justify-between my-5">
      <div class="flex gap-1 items-center">
        <img class="w-[30px]" src={logo}>
        <span class="font-extrabold pl-1 pr-3 text-2xl">Explorama</span>
        {@render navButton("Home", true)}
        {@render navButton("Showcase", false)}
        {@render navButton("Pricing", false)}
      </div>
      <img class="w-[30px] opacity-70" src="{github}">
    </nav>
  </div>
</div>

<div class="bg-black/93 text-white w-screen h-screen flex relative
            justify-center items-center overflow-y-auto flex-col">
  <!-- Main Container -->
  <div class="w-[980px] p-5 z-1 h-full">
    {@render children()}
  </div>
  
  <!-- Grid Container -->
  <div class="absolute z-0 top-0 bottom-20 w-full
              max-w-[1380px] opacity-80">
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

