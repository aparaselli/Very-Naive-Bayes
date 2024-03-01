<!-- Layout.svelte -->
<script>
  import { onMount } from "svelte";
  import * as d3 from "d3";

  export let currentVisualization;
  export let switchVisualization;

  let selectedPageIndex = 0;

  const pages = [
    { label: "Page 1", value: "Page1.svelte" },
    { label: "Page 2", value: "Page2.svelte" },
    { label: "Page 3", value: "Page3.svelte" },
    { label: "Page 4", value: "Page4.svelte" },
  ];

  onMount(() => {
    // Use D3 to bind data to dropdown options
    const select = d3.select("#pageSelect");
    select
      .selectAll("option")
      .data(pages)
      .enter()
      .append("option")
      .text((d) => d.label)
      .attr("value", (d) => d.value);
  });

  function switchToNextPage() {
    selectedPageIndex = (selectedPageIndex + 1) % pages.length;
    switchVisualization(pages[selectedPageIndex].value); // Call switchVisualization function with the selected page
  }
</script>

<div
  style="position: fixed; top: 0; left: 0; right: 0; z-index: 1000; background-color: #fff; padding: 10px;"
>
  <!-- Dropdown menu -->
  <select id="pageSelect" on:change={switchToNextPage}>
    <!-- Options will be populated dynamically using D3 -->
  </select>
</div>

<!-- Clickable area to switch pages -->
<div on:click={switchToNextPage} style="cursor: pointer;">
  <!-- Dynamic component to switch between Svelte files -->
  {#if currentVisualization}
    <svelte:component this={currentVisualization} />
  {/if}
</div>
