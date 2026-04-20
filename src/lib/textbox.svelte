<script lang="ts">
  import type { Snippet } from "svelte";

  interface Props {
    title: string
    blocks: string[]
    children?: Snippet
  }

  let {
    title,
    blocks,
    children
  }: Props = $props();

</script>

<div class="w-full flex justify-center">
  <div class="w-5/6 flex flex-col bg-zinc-900 rounded-xl py-5 px-15 gap-3
              border border-zinc-800 shadow-md/20 shadow-zinc-700">
    <span class="font-semibold text-3xl text-center">
      {title}
    </span>
    {#each blocks as block, index (index)}
      <span class="text-balanced text-xl text-center">
        {block}
      </span>
    {/each }
    {#if children}
      <span class="text-balanced text-xl text-center">
        {@render children()}
      </span>
    {/if}
  </div>
</div>
