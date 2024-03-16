<!-- OverlappingCircles.svelte -->
<script>
  // You can define any additional logic here if needed
</script>

<main>
  <h1>P(A ∩ B): Probability of A and B</h1>

  <p>As we can see below, the outcomes A and B have an overlapping section. In this overlapping section both outcomes A and B simutenously occur.
    For example if we were rolling a dice the outcome that the number is less than 3 and even have an overlapping section (the number 2). 
  </p>
  <svg width="1000" height="500">
    <!-- Blue circle with center at (200, 200) and radius of 150 -->
    <circle class="blue" cx="400" cy="250" r="200">
    <title>Probability of A</title>
    </circle>
    <!-- Green circle with center at (250, 250) and radius of 150 -->
    <circle class="green" cx="600" cy="250" r="200">
    <title>Probability of B</title>
    </circle>
    <path d="M500,423.2 A200,200, 0 0 1,500,76.759 A200,200, 0 0 0,500,76.759 A200,200, 0 0 1,500,423.2" stroke='royalblue' fill='royalblue'>
    <title>Probability of A and B</title>
    </path>
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
  circle.blue {
    fill: #ADD8E6;
    opacity: 0.4;
  }

  circle.green {
    fill: #90EE90;
    opacity: 0.4;
  }

  #svgContainer3 {
  margin-left: 510px; /* Adjust the value as needed */
  margin-top: 133px;
  }

</style>