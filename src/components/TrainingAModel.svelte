<!-- LargeBlueCircle.svelte -->
<script>
  import weightedArrow from "$lib/assets/Arrow_W_Weights.png";
  import Cog from "$lib/assets/cog.png";

  // You can define any additional logic here if needed
</script>

<main>
  <h1>Fitting a Model</h1>

  <p>
    Fitting refers to the act of optimizing a model given training data to make
    the best prediction. There are many different type of Naive Bayes models,
    and all of them have different fitting proccesses. In our example, we are
    fitting a Naive Bayes model that assigns weights to features. To predict
    ripeness, the equation becomes P(ripe | color ∩ softness) ∝ P(ripe) *
    [weight1 * P(color | ripe)] * [weight2 * P(softness | ripe)]. Using
    algorithims and mathematical techniques we adjust weight1 and weight2 during
    fitting to maximize correct predictions on our data.
  </p>

  <svg id="svgContainer" width="30%" height="auto"  viewBox="0 0 800 500">
    <g id="cogContainer">
      <image href={Cog} width="100" x="650" y="10" class="rotate" />
    </g>
    <g id="ripe">
      <circle cx="200" cy="100" r="10"></circle>
      <circle cx="200" cy="150" r="10"></circle>
      <circle cx="200" cy="200" r="10"></circle>
      <circle cx="200" cy="250" r="10"></circle>

      <circle cx="250" cy="100" r="10"></circle>
      <circle cx="250" cy="150" r="10"></circle>
      <circle cx="250" cy="200" r="10"></circle>
      <circle cx="250" cy="250" r="10"></circle>

      <circle class="soft" cx="300" cy="100" r="10"></circle>
      <circle class="soft" cx="300" cy="150" r="10"></circle>
      <circle cx="300" cy="200" r="10"></circle>
      <circle cx="300" cy="250" r="10"></circle>

      <circle class="soft" cx="350" cy="100" r="10"></circle>
      <circle class="soft" cx="350" cy="150" r="10"></circle>
      <circle cx="350" cy="200" r="10"></circle>
      <circle cx="350" cy="250" r="10"></circle>

      <circle class="greenblack-soft" cx="400" cy="100" r="10"></circle>
      <circle class="greenblack-soft" cx="400" cy="150" r="10"></circle>
      <circle class="greenblack" cx="400" cy="200" r="10"></circle>
      <circle cx="400" cy="250" r="10"></circle>

      <circle class="greenblack-soft" cx="450" cy="100" r="10"></circle>
      <circle class="greenblack-soft" cx="450" cy="150" r="10"></circle>
      <circle class="greenblack" cx="450" cy="200" r="10"></circle>
      <circle cx="450" cy="250" r="10"></circle>
    </g>
    <g id="unripe">
      <polygon class="greenblack" points="490, 108 500, 91 510, 108"></polygon>
      <polygon class="greenblack" points="490, 158 500, 141 510, 158"></polygon>
      <polygon class="greenblack" points="490, 208 500, 191 510, 208"></polygon>
      <polygon class="greenblack" points="490, 258 500, 241 510, 258"></polygon>

      <polygon class="greenblack" points="540, 108 550, 91 560, 108"></polygon>
      <polygon class="greenblack" points="540, 158 550, 141 560, 158"></polygon>
      <polygon class="greenblack" points="540, 208 550, 191 560, 208"></polygon>
      <polygon class="greenblack" points="540, 258 550, 241 560, 258"></polygon>
      <!-- Smoothed point -->
      <polygon class="smooth" points="570, 308 580, 291 590, 308"></polygon>

      <polygon points="590, 108 600, 91 610, 108"></polygon>
      <polygon points="590, 158 600, 141 610, 158"></polygon>
      <polygon points="590, 208 600, 191 610, 208"></polygon>
      <polygon points="590, 258 600, 241 610, 258"></polygon>

      <polygon points="640, 108 650, 91 660, 108"></polygon>
      <polygon points="640, 158 650, 141 660, 158"></polygon>
      <polygon points="640, 208 650, 191 660, 208"></polygon>
      <polygon points="640, 258 650, 241 660, 258"></polygon>
    </g>
    <rect
      x="175"
      y="70"
      width="510"
      height="245"
      fill="none"
      stroke="black"
      stroke-width="2"
    />
  </svg>

  <img alt="arrow" id="arrow" src={weightedArrow} />

  <!-- Trained model -->
  <svg id="svgContainer4" width="30%" height="auto" class="fade-in" viewBox="0 0 800 500">
    <rect
      x="175"
      y="70"
      width="510"
      height="245"
      fill="pink"
      stroke="black"
      stroke-width="2"
    />
    <g id="cogContainer">
      <image href={Cog} width="100" x="650" y="10" />
      <image href={Cog} width="100" x="105" y="10" />
    </g>
    <g id="ripe">
      <circle cx="200" cy="100" r="10"></circle>
      <circle cx="200" cy="150" r="10"></circle>
      <circle cx="200" cy="200" r="10"></circle>
      <circle cx="200" cy="250" r="10"></circle>

      <circle cx="250" cy="100" r="10"></circle>
      <circle cx="250" cy="150" r="10"></circle>
      <circle cx="250" cy="200" r="10"></circle>
      <circle cx="250" cy="250" r="10"></circle>

      <circle class="soft" cx="300" cy="100" r="10"></circle>
      <circle class="soft" cx="300" cy="150" r="10"></circle>
      <circle cx="300" cy="200" r="10"></circle>
      <circle cx="300" cy="250" r="10"></circle>

      <circle class="soft" cx="350" cy="100" r="10"></circle>
      <circle class="soft" cx="350" cy="150" r="10"></circle>
      <circle cx="350" cy="200" r="10"></circle>
      <circle cx="350" cy="250" r="10"></circle>

      <circle class="greenblack-soft" cx="400" cy="100" r="10"></circle>
      <circle class="greenblack-soft" cx="400" cy="150" r="10"></circle>
      <circle class="greenblack" cx="400" cy="200" r="10"></circle>
      <circle cx="400" cy="250" r="10"></circle>

      <circle class="greenblack-soft" cx="450" cy="100" r="10"></circle>
      <circle class="greenblack-soft" cx="450" cy="150" r="10"></circle>
      <circle class="greenblack" cx="450" cy="200" r="10"></circle>
      <circle cx="450" cy="250" r="10"></circle>
    </g>
    <g id="unripe">
      <polygon class="greenblack" points="490, 108 500, 91 510, 108"></polygon>
      <polygon class="greenblack" points="490, 158 500, 141 510, 158"></polygon>
      <polygon class="greenblack" points="490, 208 500, 191 510, 208"></polygon>
      <polygon class="greenblack" points="490, 258 500, 241 510, 258"></polygon>

      <polygon class="greenblack" points="540, 108 550, 91 560, 108"></polygon>
      <polygon class="greenblack" points="540, 158 550, 141 560, 158"></polygon>
      <polygon class="greenblack" points="540, 208 550, 191 560, 208"></polygon>
      <polygon class="greenblack" points="540, 258 550, 241 560, 258"></polygon>
      <!-- Smoothed point -->
      <polygon class="smooth" points="570, 308 580, 291 590, 308"></polygon>

      <polygon points="590, 108 600, 91 610, 108"></polygon>
      <polygon points="590, 158 600, 141 610, 158"></polygon>
      <polygon points="590, 208 600, 191 610, 208"></polygon>
      <polygon points="590, 258 600, 241 610, 258"></polygon>

      <polygon points="640, 108 650, 91 660, 108"></polygon>
      <polygon points="640, 158 650, 141 660, 158"></polygon>
      <polygon points="640, 208 650, 191 660, 208"></polygon>
      <polygon points="640, 258 650, 241 660, 258"></polygon>
    </g>
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
  #arrow {
    position: relative; /* Position the element absolutely */
    width: 200px;
    padding-bottom: 8%;
    opacity: 0; /* Initially hide the image */
    animation: fadeInImg 5s forwards; /* Apply the fadeIn animation */
    animation-delay: 2s;
  }
  @keyframes fadeInImg {
    from {
      opacity: 0; /* Start with opacity 0 */
    }
    to {
      opacity: 1; /* End with opacity 1 */
    }
  }
  .greenblack {
    fill: #6cb4ee;
  }
  .smooth {
    fill: #f0e68c;
    stroke: red;
  }

  @keyframes fadeIn {
    from {
      opacity: 0; /* Start with opacity 0 */
    }
    to {
      opacity: 1; /* End with opacity 1 */
    }
  }

  #cogContainer {
    transform-origin: center;
    border: 2px solid black; /* Add a black border around the container */
    width: 100px; /* Set the width to match the cog image */
    height: 100px; /* Set the height to match the cog image */
    position: relative; /* Ensure proper positioning */
  }

  #svgContainer {
    padding-left: 10%;
  }
  #weight {
    display: inline-block;
    position: relative;

  }

  #svgContainer4 {
    position: relative; /* Position the element absolutely */
  }

  circle {
    fill: None;
    stroke: black;
  }
  .soft {
    fill: #f0e68c;
  }
  .greenblack-soft {
    fill: #6deb86;
  }
  .greenblack {
    fill: #6cb4ee;
  }

  polygon {
    fill: None;
    stroke: black;
  }

  @keyframes rotate {
    from {
      transform: rotate(0deg); /* Start rotation from 0 degrees */
    }
    to {
      transform: rotate(360deg); /* End rotation at 360 degrees */
    }
  }

  .rotate {
    width: 100px; /* Set the desired width */
    height: auto;
    animation: rotate 6s linear; /* Apply rotation animation */
    transform-origin: 50% 50%;
    transform-box: fill-box;
  }

  .fade-in {
    opacity: 0; /* Initially hide the SVG */
    animation: fadeIn 5s forwards; /* Apply the fadeIn animation */
    animation-delay: 2s;
  }

  @keyframes fadeIn {
    from {
      opacity: 0; /* Start with opacity 0 */
    }
    to {
      opacity: 1; /* End with opacity 1 */
    }
  }

  .fade-in2 {
    opacity: 0; /* Initially hide the SVG */
    animation: fadeIn2 4s forwards; /* Apply the fadeIn animation */
    animation-delay: 3s;
  }

  @keyframes fadeIn2 {
    from {
      opacity: 0; /* Start with opacity 0 */
    }
    to {
      opacity: 1; /* End with opacity 1 */
    }
  }
</style>
