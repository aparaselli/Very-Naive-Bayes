<!-- Layout.svelte -->
<script>
  import { onMount, onDestroy } from "svelte";

  export let currentVisualization;
  export let switchVisualization;

  let selectedPageIndex = 0;
  let isDragging = false;

  const pages = [
    { label: "Intro", value: "Page0.svelte" },
    { label: "Page 1", value: "Page1.svelte" },
    { label: "Page 2", value: "Page2.svelte" },
    { label: "Page 3", value: "Page3.svelte" },
    { label: "Page 4", value: "Page4.svelte" },
    { label: "test", value: "Page5.svelte" },
    { label: "Page 6", value: "Page6.svelte" },
    { label: "Page 7", value: "Page7.svelte" },
    { label: "Page 8", value: "Page8.svelte" },
    { label: "Page 9", value: "Page9.svelte" },
    { label: "Page 10", value: "Page10.svelte" },
    { label: "Page 11", value: "Page11.svelte" },
    { label: "Page 12", value: "Page12.svelte" },
    { label: "Page 13", value: "Page13.svelte" }
  ];

  // for the arrows
  function switchToNextPage() {
    selectedPageIndex = (selectedPageIndex + 1) % pages.length;
    switchVisualization(pages[selectedPageIndex].value);
    console.log('forward')
    console.log(selectedPageIndex)
  }

  function switchToPreviousPage() {
    selectedPageIndex = (selectedPageIndex - 1 + pages.length) % pages.length;
    switchVisualization(pages[selectedPageIndex].value);
    console.log('back')
    console.log(selectedPageIndex)
  }

  // for the slider
  function switchToPage(index) {
    selectedPageIndex = index;
    switchVisualization(pages[selectedPageIndex].value);
  }

  function handleMouseDown(event) {
    isDragging = true;
    handleMouseMove(event);
  }

  function handleMouseMove(event) {
    if (isDragging) {
      const sliderWidth = document.getElementById("slider").offsetWidth;
      const position = event.clientX - document.getElementById("slider").getBoundingClientRect().left;
      let percentage = position / sliderWidth;
      percentage = Math.min(1, Math.max(0, percentage)); // Clamp percentage between 0 and 1
      selectedPageIndex = Math.round(percentage * (pages.length - 1));
      
      switchVisualization(pages[selectedPageIndex].value);
    }
  }

  function handleMouseUp() {
    isDragging = false;
  }

  function handleMouseLeave() {
    isDragging = false;
  }
</script>

<style>
  .arrow {
    transition: transform 0.2s;
    width: 0;
    height: 0;
    border-top: 10px solid transparent;
    border-bottom: 10px solid transparent;
    cursor: pointer;
  }

  #left {
    border-right: 15px solid grey;
    transform: rotate(180deg);
  }

  #right {
    border-left: 15px solid black;
  }

  .arrow:hover {
    transform: scale(1.5);
  }

  .slider {
    width: 80%;
    height: 5px;
    background-color: #ddd;
    position: fixed;
    top: 820px;
    left: 50%;
    transform: translateX(-50%);
    border-radius: 5px;
    cursor: pointer;
  }

  .slider-progress {
    height: 100%;
    background-color: #1e4d80;
    border-radius: 5px;
  }

  .circle-button {
    width: 20px;
    height: 20px;
    border-radius: 50%;
    background-color: #1e4d80;
    position: absolute;
    top: 50%;
    transform: translate(-50%, -50%);
    z-index: 1;
    cursor: pointer;
  }
</style>

<div
  id="left"
  class="arrow"
  style="position: fixed; top: 50%; left: 60px; transform: translateY(-50%);"
  on:click={switchToPreviousPage}
></div>

<div
  id="right"
  class="arrow"
  style="position: fixed; top: 50%; right: 60px; transform: translateY(-50%);"
  on:click={switchToNextPage}
></div>

<div
  id="slider"
  class="slider"
  on:mousemove={handleMouseMove}
  on:mousedown={handleMouseDown}
  on:mouseup={handleMouseUp}
  on:mouseleave={handleMouseLeave}
>
  <div class="slider-progress" style="width: {(selectedPageIndex / (pages.length - 1)) * 100}%;"></div>
  <div class="circle-button" style="left: {(selectedPageIndex / (pages.length - 1)) * 100}%;" on:click={() => switchToPage(selectedPageIndex)}></div>
</div>

<!-- Dynamic component to switch between Svelte files -->
{#if currentVisualization}
  <svelte:component this={currentVisualization} />
{/if}
