<script lang="ts">
	import './layout.css';
	import logo from '$lib/assets/logo.svg';

	let { children } = $props();
</script>

<svelte:head>
  <link rel="icon" href={logo} />
</svelte:head>

{#snippet navButton(text: string, isOpen: boolean)}
  <div class="flex align-center px-1 {isOpen ? 'border-b-2 border-white' : ''}">
    {text} 
  </div>
{/snippet}

<nav class="bg-black text-white flex p-2 my-2 mx-10 rounded-xl font-bold gap-10 justify-center shadow-lg shadow-gray-500/20">
  {@render navButton("Home", true)}
  {@render navButton("Showcase", false)}
  {@render navButton("Pricing", false)}
</nav>

{@render children()}

<!-- background grid -->
<div class="bg-gray-light w-full h-full absolute -z-2 inset-0" />
<div class="absolute -z-1 inset-0 top-[31px] left-[31px] h-full w-full
            bg-[radial-gradient(circle,#232525ff_5px,transparent_5px)]
            bg-[size:60px_60px]" />
<div class="absolute -z-1 inset-0 h-full w-full
            bg-[linear-gradient(to_right,#232525ff_2px,transparent_2px),linear-gradient(to_bottom,#232525ff_2px,transparent_2px)]
            bg-[size:60px_60px]" />
