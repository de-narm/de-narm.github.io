<script lang="ts">
	import logo from '$lib/assets/logo.svg';
	import screenshot from '$lib/assets/screenshot.png';
</script>

<!-- Main Block -->
<div class="w-full pt-20 flex-col flex justify-center items-center gap-6 
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

  <!-- Screenshot -->
  <div class="mt-20 p-10">
    <div class="bg-zinc-950 p-4 border border-zinc-600 rounded-3xl">
      <img src={screenshot} class="rounded-2xl">
    </div>
  </div>

  <div class="mt-20 px-10 relative w-full flex items-center">
    <!-- Example frame -->
    <div class="w-[650px] h-[400px] bg-frame-bg rounded-xl overflow-hidden 
                flex flex-col">
      <!-- Header -->
      <div class="w-full h-10 flex relative">
        <div class="w-2/3 h-full bg-frame-gray flex justify-end">
          <div class="h-full w-[200px] bg-frame-fill"
               style="clip-path: path('M 0 40 Q 50 40 100 20 Q 150 0 200 0 L 200 40');"
          >
          </div>
        </div>
        <div class="w-1/3 h-full bg-frame-fill">
        </div>
        <div class="absolute left-10 top-2">
          Some title
        </div>
      </div>

      <!-- Content -->
      <div class="w-full h-full border-y-3 border-frame-fill flex items-center 
                  justify-center">
                  Some pseudo interactive frame examples maybe?
      </div>

    </div>

    <!-- Example note -->
    <div class="absolute right-0 w-[350px] h-[200px] bg-zinc-400 rounded-4xl
                flex items-center justify-center text-black">
      Some Feature notes!
    </div>
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

