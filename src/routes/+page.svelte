<script lang="ts">
	import logo from '$lib/assets/logo.svg';
</script>

<!-- Main Block -->
<div class="w-full py-20 flex-col flex justify-center items-center gap-6 
            relative">
  <!-- Intro Text -->
  <div class="w-[400px] text-center text-5xl font-semibold z-1">
    This could be our 
    <span class="text-logo italic">awesome</span>
    motto
  </div>
  <div class="w-[300px] text-center text-2xl font-medium text-stone-300 z-1">
    Have I told you about our featuring features yet?
  </div>
  <button class="bg-logo px-5 py-3 rounded-xl z-1">
    Start now!
  </button>

  <!-- Background Grid -->
  <div class="absolute inset-0 h-full w-full opacity-60
              mask-y-from-95% mask-x-from-80%">
    <div class="absolute top-[31px] left-[31px] h-full w-full
                bg-[radial-gradient(circle,#232525ff_5px,transparent_5px)]
                bg-[size:60px_60px]" />
    <div class="absolute h-full w-full
                bg-[linear-gradient(to_right,#232525ff_2px,transparent_2px),linear-gradient(to_bottom,#232525ff_2px,transparent_2px)]
                bg-[size:60px_60px]" />
  </div>
</div>

<!--
{#snippet transition(startColor: string, endColor: string, rotate: boolean = false)}
  <div class="w-full h-[50px] flex bg-{startColor} {rotate ? 'rotate-180' : ''}">
    <div class="h-full w-full "></div>
    <div class="h-full min-w-[600px] max-w-[600px] bg-{endColor}"
         style="clip-path: path('M 0 50 Q 150 50 300 25 Q 450 0 600 0 L 600 50');"
    ></div>
    <div class="h-full w-full bg-{endColor}"></div>
  </div>
{/snippet}

{#snippet colorBlock(color: string)}
  <div>
  {@render transition("transparent", color)}
  <div class="w-full h-[200px] bg-{color}">
  </div>
  {@render transition("transparent", color, true)}
  </div>
{/snippet}

<div class="flex justify-center">
  <img class="w-1/3 m-10" src={logo} />
</div>

{@render colorBlock("purple-logo")}

<div class="flex justify-center">
  <img class="w-1/3 m-10" src={logo} />
</div>

{@render colorBlock("black")}

<div class="flex justify-center">
  <img class="w-1/3 m-10" src={logo} />
</div>


*** background grid
<div class="bg-gray-light w-full h-full absolute -z-2 inset-0" />
<div class="absolute -z-1 inset-0 top-[31px] left-[31px] h-full w-full
            bg-[radial-gradient(circle,#232525ff_5px,transparent_5px)]
            bg-[size:60px_60px]" />
<div class="absolute -z-1 inset-0 h-full w-full
            bg-[linear-gradient(to_right,#232525ff_2px,transparent_2px),linear-gradient(to_bottom,#232525ff_2px,transparent_2px)]
            bg-[size:60px_60px]" />
-->

