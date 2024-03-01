<!-- OverlappingCircles.svelte -->
<script>
  // You can define any additional logic here if needed
</script>

<main>
  <h1 style="margin-top: 50px;">P(A ∩ B): Probability of A and B</h1>

  <p>
    As we can see below, the outcomes A and B have an overlapping section. In
    this overlapping section both outcomes A and B simutenously occur. For
    example if we were rolling a dice the outcome that the number is less than 3
    and even have an overlapping section (the number 2).
  </p>
</main>

<svg width="1600" height="1600">
  <!-- Blue circle with center at (200, 200) and radius of 150 -->
  <circle class="blue" cx="400" cy="400" r="200">
    <title>Probability of A</title>
  </circle>
  <!-- Green circle with center at (250, 250) and radius of 150 -->
  <circle class="green" cx="600" cy="400" r="200">
    <title>Probability of B</title>
  </circle>
  <path
    d="M500,573.2 A200,200, 0 0 1,500,226.8 A200,200, 0 0 0,500,226.8 A200,200, 0 0 1,500,573.2"
    stroke="royalblue"
    fill="royalblue"
  >
    <title>Probability of A and B</title>
  </path>
</svg>

<style>
  /* Style the SVG circle elements */
  circle.blue {
    fill: #add8e6;
    opacity: 0.4;
  }

  circle.green {
    fill: #90ee90;
    opacity: 0.4;
  }
</style>
