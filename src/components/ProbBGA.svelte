<!-- OverlappingCircles.svelte -->
<script>
  // You can define any additional logic here if needed
</script>

<main>
  <h1>P(A|B): Probability of B given A</h1>

  <h3>
    Now that we know A and B have an overlapping section, another thing we may
    ask is that if we observed A what is the chance that we also observed B.
    This is called conditional probability and we define the probability of B
    given A as P(A ∩ B)&divideP(A).
  </h3>
</main>

<svg width="700" height="700">
  <!-- Blue circle with center at (200, 200) and radius of 150 -->
  <circle class="blue" cx="400" cy="400" r="200">
    <title>Probability of A</title>
  </circle>
  <path
    d="M500,573.2 A200,200, 0 0 1,500,226.8 A200,200, 0 0 0,500,226.8 A200,200, 0 0 1,500,573.2"
    stroke="royalblue"
    fill="royalblue"
  >
    <title>Probability of B given A</title>
  </path>
</svg>
<svg height="500" width="50%">
  <text x="1800" y="200" fill="red" font-size="35">I love SVG!</text>
</svg>

<style>
  /* Style the SVG circle elements */
  circle.blue {
    fill: #add8e6;
    opacity: 0.4;
  }
  h1 {
    margin-top: 50px;
  }
  h3 {
    color: grey;
  }
</style>
