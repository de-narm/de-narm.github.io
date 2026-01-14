<script lang="ts">
	import './layout.css';
	import logo from '$lib/assets/logo.svg';

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

<div class="bg-black text-white w-screen h-screen flex 
            justify-center overflow-y-hidden">
  <div class="w-[980px] p-5">
    <nav class="flex justify-between my-5">
      <div class="flex gap-1 items-center">
        <img class="w-[30px]" src={logo}>
        <span class="font-extrabold pl-1 pr-3 text-2xl">Explorama</span>
        {@render navButton("Home", true)}
        {@render navButton("Showcase", false)}
        {@render navButton("Pricing", false)}
      </div>
      <div class="">
      </div>
    </nav>
    {@render children()}
  </div>
</div>

