<script lang="ts">
  import { onMount } from "svelte";
  import Element, { type ElementData } from "./Element.svelte";

  let values: ElementData[] = [
    { data: 1, value: "one" },
    { data: 2, value: "two" },
    { data: 3, value: "three" },
  ];

  onMount(() => {
    setTimeout(() => {
      values[1] = { data: 4, value: "four" };
      values = values;
    }, 400);
  });
</script>

{#each values as value (value.value)}
  <Element {value} />
{/each}
