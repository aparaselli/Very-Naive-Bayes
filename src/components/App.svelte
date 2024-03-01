<script>
<<<<<<< Updated upstream
  // Write your JS here, or import other files
=======
  import { onMount } from "svelte";
  import Page1 from "./ProbA.svelte";
  import Page2 from "./ProbB.svelte";
  import Page3 from "./ProbAB.svelte";
  import Page4 from "./ProbBGA.svelte";
  import Layout from "./Layout.svelte";

  let currentVisualization = Page1; // Initial visualization is Page1

  function switchVisualization(page) {
    switch (page) {
      case "Page1.svelte":
        currentVisualization = Page1;
        break;
      case "Page2.svelte":
        currentVisualization = Page2;
        break;
      case "Page3.svelte":
        currentVisualization = Page3;
        break;
      case "Page4.svelte":
        currentVisualization = Page4;
        break;
      default:
        break;
    }
  }
>>>>>>> Stashed changes
</script>

<main>
  <h1>Svelte template</h1>

  <p>Write your HTML here</p>
</main>

<style>
  /* Write your CSS here */
</style>
