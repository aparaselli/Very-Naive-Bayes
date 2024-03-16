<!-- LargeBlueCircle.svelte -->
<script>
  // You can define any additional logic here if needed
</script>

<main>
  <h1>P(A): Probability of A</h1>

  <p>
    When an event happens we observe outcomes. For example when we flip a coin
    we observe that it lands heads or tails. Similarly, when we roll a dice we
    observe a number. Here the blue circle represents the probability of
    observing the outcome A for an arbitrary event.
  </p>

  <svg width="1000" height="500">
    <!-- Define a circle element with a radius of 80 -->
    <circle cx="400" cy="250" r="200">
      <title>Probability space for event A</title>
    </circle>
  </svg>

  <!-- SVG for BG -->
    <svg id="svgContainer3" width="400" height="100" xmlns="http://www.w3.org/2000/svg">
    <!-- Create a rectangle -->
    <rect width="200" height="50" x="1" y="25" fill="none" stroke=none stroke-width="2" />

    <!-- Add text inside the rectangle -->
    <text x="100" y="55" text-anchor="middle" alignment-baseline="middle" font-family="Arial" font-size="20" fill="black"> </text>
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
    background-color: beige;
    margin: 0;
    padding: 0;
  }
  circle {
    fill: #add8e6;
    opacity: 0.8;
  }

  #svgContainer3 {
  margin-left: 510px; /* Adjust the value as needed */
  margin-top: 133px;
  }
</style>
