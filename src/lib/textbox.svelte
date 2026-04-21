<script lang="ts">
  import type { Snippet } from "svelte";

  interface Props {
    title: string
    blocks: string[] | [string, string][]
    children?: Snippet
  }

  let {
    title,
    blocks,
    children
  }: Props = $props();

</script>

<div class="w-full flex justify-center px-10">
  <div class="w-full flex flex-col bg-zinc-900 rounded-xl py-5 px-10 gap-3
              border border-zinc-800 shadow-md/20 shadow-zinc-700">
    <span class="font-semibold text-xl">
      {title}
    </span>
    {#each blocks as block, index (index)}
      {#if (typeof block === "string")}
        <span class="text-balanced text-md text-zinc-300">
          {block}
        </span>
      {:else}
        <div class="flex lg:flex-row flex-col">
          <span class="text-balanced text-md font-semibold lg:w-2/6">
            {block[0]}
          </span>
          <span class="text-balanced text-md text-zinc-300 w-full">
            {block[1]}
          </span>
        </div>
      {/if}
    {/each }
    {#if children}
      <span class="text-balanced text-md text-zinc-300">
        {@render children()}
      </span>
    {/if}
  </div>
</div>
