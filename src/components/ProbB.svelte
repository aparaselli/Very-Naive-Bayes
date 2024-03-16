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

  circle {
    fill: #90EE90;
    opacity: 0.8;
  }
</style>

