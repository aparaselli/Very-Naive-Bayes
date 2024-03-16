<!-- LargeBlueCircle.svelte -->
<script>
  // You can define any additional logic here if needed
  const videoUrl = 'https://www.youtube.com/embed/W_0_tD0sZWs&ab_channel';
</script>

<main>
  <h1>Predicting The Unknown Using <s>Magic</s> Math</h1>
  <p> An explanation of how simple math and observation can be coupled to use the naive bayes classification technique to make predictions </p>

  <!-- SVG for BG -->
    <svg id="svgContainer3" width="400" height="100" xmlns="http://www.w3.org/2000/svg">
    <!-- Create a rectangle -->
    <rect width="200" height="50" x="1" y="25" fill=none stroke=none stroke-width="2" />

    <!-- Add text inside the rectangle -->
    <text x="100" y="55" text-anchor="middle" alignment-baseline="middle" font-family="Arial" font-size="20" fill="black"> </text>
    </svg>

      <!-- SVG for blocking -->
    <svg id="svgContainer2" width="400" height="100" xmlns="http://www.w3.org/2000/svg">
    <!-- Create a rectangle -->
    <rect width="200" height="50" x="1" y="25" fill=none stroke=none stroke-width="2" />

    <!-- Add text inside the rectangle -->
    <text x="100" y="55" text-anchor="middle" alignment-baseline="middle" font-family="Arial" font-size="20" fill="black"> </text>
    </svg>
  
    <div class="video-container">
    <iframe
      width="560"
      height="415"
      src="https://www.youtube.com/embed/W_0_tD0sZWs"
      frameborder="0"
      allowfullscreen
    ></iframe>
  </div>


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
    text-align: center; /* Center-align the text */
  }

  #svgContainer3 {
  margin-left: 110px; /* Adjust the value as needed */
  margin-top: 664px;
  }



  .video-container {
    position: absolute; /* Change to absolute positioning */
    top: 50%; /* Position it 50% from the top */
    left: 50%; /* Position it 50% from the left */
    transform: translate(-50%, -50%); /* Center the element */
  }

  .video-container iframe {
    width: 1500px; /* Set a specific width */
    height: 600px; /* Set a specific height */
  }

</style>
