<!-- OverlappingCircles.svelte -->
<script>
  // You can define any additional logic here if needed
</script>

<main>
  <h1>P(B|A): Probability of B given A</h1>

  <p>Now that we know A and B have an overlapping section, this can also be understood as the probability of event B happening if event A has happened.
  This is called conditional probability and we define the probability of B given A as P(A ∩ B)&divideP(A).

  </p>
  <svg width="1000" height="500">
    <!-- Blue circle with center at (200, 200) and radius of 150 -->
    <circle class="blue" cx="400" cy="250" r="200">
    <title>Probability of A</title>
    </circle>
    <path d="M500,423.2 A200,200, 0 0 1,500,76.759 A200,200, 0 0 0,500,76.759 A200,200, 0 0 1,500,423.2" stroke='royalblue' fill='royalblue'>
      <title>Probability of B given A</title>
    </path>
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

  circle.blue {
    fill: #ADD8E6;
    opacity: 0.4;
  }
</style>