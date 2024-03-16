<!-- LargeBlueCircle.svelte -->
<script>
  // You can define any additional logic here if needed
</script>

<main>
  <h1>P(A): Probability of A</h1>

  <p>
    When an event happens we observe outcomes! Here the blue circle represents the probability of
    observing outcome A for an arbitrary event.
  </p>

  <svg width="1000" height="500">
    <!-- Define a circle element with a radius of 80 -->
    <circle cx="400" cy="250" r="200">
      <title>Probability space for event A</title>
    </circle>
  </svg>
</main>

<style>
  h1 {
    padding-left: 188px;
    padding-top: 10px;
    padding-right: 188px;
    font-family: Arial, Helvetica, sans-serif;
  }
  p {
    padding-left: 188px;
    padding-right: 188px;
    font-family: Arial, Helvetica, sans-serif;
        font-size: 18px; /* Increase font size */
        line-height: 1.5; /* Double-spaced text */
  }
  main {
    margin: 0;
    padding: 0;
  }
  circle {
    fill: #add8e6;
    opacity: 0.8;
  }
</style>
