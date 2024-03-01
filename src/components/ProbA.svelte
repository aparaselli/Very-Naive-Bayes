<!-- LargeBlueCircle.svelte -->
<script>
  // You can define any additional logic here if needed
</script>

<main>
  <h1 style="margin-top: 50px;">P(A): Probability of A</h1>

  <p>
    When an event happens we observe outcomes. For example when we flip a coin
    we observe that it lands heads or tails. Similarly, when we roll a dice we
    observe a number. Here the blue circle represents the probability of
    observing the outcome A for an arbitrary event.
  </p>
</main>

<svg width="1600" height="1600">
  <!-- Define a circle element with a radius of 80 -->
  <circle cx="400" cy="400" r="200">
    <title>Probability space for event A</title>
  </circle>
</svg>

<style>
  /* Style the SVG circle element */
  circle {
    fill: #add8e6;
    opacity: 0.8;
  }
</style>
