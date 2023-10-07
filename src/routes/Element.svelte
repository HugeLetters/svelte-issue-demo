<!-- <svelte:options immutable /> -->

<script
  lang="ts"
  context="module"
>
  export type ElementData = { value: string; data: number };
</script>

<script lang="ts">
  export let value: ElementData;

  $: {
    console.log("value changed", value.data, value.value);
  }
</script>

<div>{value.data} - {value.value}</div>
