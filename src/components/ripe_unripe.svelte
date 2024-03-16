<!-- OverlappingCircles.svelte -->
<script>
  import Icon from "$lib/assets/icon.jpg";
  import dancing from "$lib/assets/couple.jpg";
</script>

<main>
  <h1>Classifying an Avocado</h1>
  <p>
    Say we were given an avocado <span><img src={Icon} alt="download icon" /></span> called Avi and we wanted to classify whether it was ripe
    or unripe. 
    While we don't know the true chance of an avocado being ripe or not given its color, we can use a bag of avocado to estimate the conditional probabilities!
  </p>
 
  <svg width="1000" height="450">
    <text class="label" x="250" y="50">P(ripe) = 24 / 50</text>
    <text x="40" y="24.2" transform="rotate(270, 40, 120) scale(2,20)">}</text>
    <circle cx="200" cy="100" r="10"></circle>
    <circle cx="200" cy="150" r="10"></circle>
    <circle cx="200" cy="200" r="10"></circle>
    <circle cx="200" cy="250" r="10"></circle>

    <circle cx="250" cy="100" r="10"></circle>
    <circle cx="250" cy="150" r="10"></circle>
    <circle cx="250" cy="200" r="10"></circle>
    <circle cx="250" cy="250" r="10"></circle>

    <circle cx="300" cy="100" r="10"></circle>
    <circle cx="300" cy="150" r="10"></circle>
    <circle cx="300" cy="200" r="10"></circle>
    <circle cx="300" cy="250" r="10"></circle>

    <circle cx="350" cy="100" r="10"></circle>
    <circle cx="350" cy="150" r="10"></circle>
    <circle cx="350" cy="200" r="10"></circle>
    <circle cx="350" cy="250" r="10"></circle>

    <circle cx="400" cy="100" r="10"></circle>
    <circle cx="400" cy="150" r="10"></circle>
    <circle cx="400" cy="200" r="10"></circle>
    <circle cx="400" cy="250" r="10"></circle>

    <circle cx="450" cy="100" r="10"></circle>
    <circle cx="450" cy="150" r="10"></circle>
    <circle cx="450" cy="200" r="10"></circle>
    <circle cx="450" cy="250" r="10"></circle>

    <text class="label" x="500" y="50">P(unripe) = 16 / 50</text>
    <text x="40" y="63.5" transform="rotate(270, 40, 120) scale(2,11)">}</text>
    <polygon points="490, 108 500, 91 510, 108"></polygon>
    <polygon points="490, 158 500, 141 510, 158"></polygon>
    <polygon points="490, 208 500, 191 510, 208"></polygon>
    <polygon points="490, 258 500, 241 510, 258"></polygon>

    <polygon points="540, 108 550, 91 560, 108"></polygon>
    <polygon points="540, 158 550, 141 560, 158"></polygon>
    <polygon points="540, 208 550, 191 560, 208"></polygon>
    <polygon points="540, 258 550, 241 560, 258"></polygon>

    <polygon points="590, 108 600, 91 610, 108"></polygon>
    <polygon points="590, 158 600, 141 610, 158"></polygon>
    <polygon points="590, 208 600, 191 610, 208"></polygon>
    <polygon points="590, 258 600, 241 610, 258"></polygon>

    <polygon points="640, 108 650, 91 660, 108"></polygon>
    <polygon points="640, 158 650, 141 660, 158"></polygon>
    <polygon points="640, 208 650, 191 660, 208"></polygon>
    <polygon points="640, 258 650, 241 660, 258"></polygon>
    
  </svg>
  <img id='couple' src={dancing} alt="dancing avocados"/>

  <!-- SVG for BG -->
    <svg id="svgContainer3" width="400" height="100" xmlns="http://www.w3.org/2000/svg">
    <!-- Create a rectangle -->
    <rect width="200" height="50" x="1" y="25" fill="none" stroke=none stroke-width="2" />

    <!-- Add text inside the rectangle -->
    <text x="100" y="55" text-anchor="middle" alignment-baseline="middle" font-family="Arial" font-size="20" fill="black"> </text>
    </svg>
</main>

<style>
  /* Style the SVG circle elements */
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
    height: 100%;
    width: 100%;
    background-color: beige;
    margin: 0;
    padding: 0;
  }
  img {
    width: 50px;
    mix-blend-mode: multiply;
  }
  #couple {
    width: 400px;
    position: absolute;
    top: 140px;
    left: 800px;
  }
  .label {
    font-size: 18px;
    font-family: Arial;
  }
  circle {
    fill: None;
    stroke: black;
  }

  polygon {
    fill: None;
    stroke: black;
  }
  #svgContainer3 {
  margin-left: 510px; /* Adjust the value as needed */
  margin-top: 140px;
  }
</style>
