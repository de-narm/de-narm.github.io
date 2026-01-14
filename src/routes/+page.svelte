<script lang="ts">
	import logo from '$lib/assets/logo.svg';
</script>

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
  {@render transition("transparent", color)}
  <div class="w-full h-[200px] bg-{color}">
  </div>
  {@render transition("transparent", color, true)}
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

