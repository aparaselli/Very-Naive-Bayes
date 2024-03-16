<!-- LargeBlueCircle.svelte -->
<script>
    import Icon from "$lib/assets/iconNoBG.png";
    import Arrow from "$lib/assets/arrow.png";
    import Cog from "$lib/assets/cog.png";
    
  // You can define any additional logic here if needed
     
</script>

<main>
  <h1>Conclusion And Takeaways</h1>

  <p>
    Now that we have a model we can make predictions about Avi and all of friends with ease! We hope that through the use of our animations,
    examples and emphasis on visuals to represent data you were able to successfully understand the basics and most importantly, the inuition behind the naive bayes classifier. You now know
    basic probility rules, the math used to make a prediction, and the methodology behind creating a naive bayes classification model. Using this knowledge
    your ready to tackle classification problems and learn more about the world of machine learning!
  </p>



  <img
      id="A"
      src={Icon}
      class = "image2"
      style="width: 200px; height: auto;"
    />
      <img
      id="A"
      src={Icon}
      class = "image"
      style="width: 200px; height: auto;"
    />
      <img
      id="A"
      src={Icon}
      class = "image"
      style="width: 200px; height: auto;"
    />





    <!-- Trained model -->
    <svg id=svgContainer width="900" height="450">
    <rect x="175" y="70" width="510" height="245" fill="pink" stroke="black" stroke-width="2" />
    <g id="cogContainer">
    <image href={Cog} width="100" x="650" y="10"/>
    <image href={Cog} width="100" x="105" y="10"/>
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

      <polygon class="greenblack" points="540, 108 550, 91 560, 108"
      ></polygon>
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

    <img
      id="B"
      src={Arrow}
      class = "image3"
      
    />

    <!-- SVG for BG -->
    <svg id="svgContainer3" width="400" height="100" xmlns="http://www.w3.org/2000/svg">
    <!-- Create a rectangle -->
    <rect width="200" height="50" x="1" y="25" fill=none stroke=none stroke-width="2" />

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
  .image {
    width: 50px; /* Set the width to the desired size */
    height: auto; /* Maintain aspect ratio */
    margin-right: 10px; /* Add right margin to create space between images */
    margin-left: 10px;
    display: inline-block;
  }

  .image2 {
    margin-right: 10px; /* Add right margin to create space between images */
    margin-left: 185px;
    margin-top: 60px;
    display: inline-block;
  }
  .image3 {
    display: inline-block;
    position: absolute;
    left: 880px; /* Adjust the horizontal position */
    top: 320px; /* Adjust the vertical position */
  }
  #A {
    width: 300px; /* Set the width to the desired smaller size */
    height: auto; /* Maintain aspect ratio */
  }
  #B {
    width: 200px; /* Set the width to the desired smaller size */
    height: auto; /* Maintain aspect ratio */
    margin-bottom:  150px;
  }
  .greenblack {
    fill: #6cb4ee;
  }
  .smooth {
    fill: #f0e68c;;
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
  .label {
    font-size: 18px;
    font-family: Arial;
  }

#cogContainer {
  transform-origin: center;
  border: 2px solid black; /* Add a black border around the container */
  width: 100px; /* Set the width to match the cog image */
  height: 100px; /* Set the height to match the cog image */
  position: relative; /* Ensure proper positioning */
}

#svgContainer {
  display: inline-block;
  position: absolute;
  left: 980px; /* Adjust the horizontal position */
  top: 195px; /* Adjust the vertical position */
 
}
#svgContainer2 {
  display: inline-block;
  position: absolute;
  left: 800px; /* Adjust the horizontal position */
  top: 259px; /* Adjust the vertical position */

}
#svgContainer3 {
  margin-left: 1050px; /* Adjust the value as needed */
  margin-top: 271px;
}

#svgContainer4 {
    position: absolute; /* Position the element absolutely */
    left: 970px; /* Set the left position */
    bottom: 315px; /* Set the bottom position */
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




</style>
