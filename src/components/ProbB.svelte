<!-- LargeBlueCircle.svelte -->
<script>
  // You can define any additional logic here if needed
</script>

<main>
  <h1 style="margin-top: 50px;">P(B): Probability of B</h1>

  <p>
    Similarly, we can label another arbitrary outcome of the event as B and this
    will be represented by the green circle.
  </p>
</main>

<svg width="1600" height="1600">
  <!-- Define a circle element with a radius of 80 -->
  <circle cx="600" cy="400" r="200">
    <title>Probability space for event B</title>
  </circle>
</svg>

<style>
  /* Style the SVG circle element */
  circle {
    fill: #90ee90;
    opacity: 0.8;
  }
</style>
