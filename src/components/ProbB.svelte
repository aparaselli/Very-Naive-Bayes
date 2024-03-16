<!-- LargeBlueCircle.svelte -->
<script>
  // You can define any additional logic here if needed
  //test
</script>

<main>
  <h1>P(B): Probability of B</h1>

  <p>Similarly, we can label another arbitrary outcome of the event as B and this will be represented by the green circle.</p>
  <svg width="1000" height="500">
    <circle cx="600" cy="250" r="200">
    <title>Probability space for event B</title>
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
    fill: #90EE90;
    opacity: 0.8;
  }

  #svgContainer3 {
  margin-left: 510px; /* Adjust the value as needed */
  margin-top: 160px;
  }
</style>

