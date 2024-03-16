<!-- LargeBlueCircle.svelte -->
<script>
    import Icon from "$lib/assets/iconNoBG.png";
    import Arrow from "$lib/assets/arrow.png";
  // You can define any additional logic here if needed
     
</script>

<main>
  <h1>Creating a Model</h1>

  <p>
    When creating models, data preparation is crucial. When observing our dataset, 
    we notice a lack of unripe soft avocados. This could lead our classifier to always predict a 
    0% chance of an avocado being unripe when soft. In this case we want to avoid such certainty, so we employ data smoothing. 
    This involves adjusting our data to prevent 0 probabilities. For this example, we'll just add one imaginary unripe soft avocado to our observed data
  </p>



   <svg id=svgContainer width="1900" height="450">
    <g id="ripe">
      <text class="label" x="313" y="50">ripe</text>
      <text x="40" y="24.2" transform="rotate(270, 40, 120) scale(2,20)">}</text
      >
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
      <text class="label" x="551" y="50">unripe</text>
      <text x="40" y="63.5" transform="rotate(270, 40, 120) scale(2,11)">}</text
      >
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
    <!-- Legend -->
    <rect x="190" y="350" width="40" height="10" fill="#6cb4ee" />
    <text x="240" y="360" font-family="Arial">Green-Black</text>
    <rect x="190" y="370" width="40" height="10" fill="#f0e68c" />
    <text x="240" y="380" font-family="Arial">Soft</text>
    <rect x="190" y="390" width="40" height="10" fill="#6deb86" />
    <text x="240" y="400" font-family="Arial">Green-Black & Soft</text>
  </svg>
    <!-- SVG for BG -->
    <svg id="svgContainer3" width="400" height="100" xmlns="http://www.w3.org/2000/svg">
    <!-- Create a rectangle -->
    <rect width="200" height="50" x="1" y="25" fill=none stroke=none stroke-width="2" />

    <!-- Add text inside the rectangle -->
    <text x="100" y="55" text-anchor="middle" alignment-baseline="middle" font-family="Arial" font-size="20" fill="black"> </text>
    </svg>


    <svg id="svgContainer2" width="1000" height="200" xmlns="http://www.w3.org/2000/svg">
        <!-- Create a rectangle -->
        <rect width="50" height="100" x="1" y="25" fill="none" stroke="none" stroke-width="2" />

        <!-- Add text inside the rectangle -->
        <text x="350" y="55" text-anchor="middle" alignment-baseline="middle" font-family="Arial" font-size="20" fill="blue" class="strikethrough"> P(unripe) * P(green-black | unripe) * P(soft | unripe) = 16/50 * 7/16 * 0/16 = 0.0
          </text>
        <line x1="0" y1="53" x2="700" y2="53" stroke="red" stroke-width="2" class="animated-strikethrough" />
    </svg>



    <svg id=corrText width="1000" height="200" xmlns="http://www.w3.org/2000/svg">
    <!-- Define the text element -->
    <text x="360" y="55" text-anchor="middle" alignment-baseline="middle" font-family="Arial" font-size="20" fill="red" opacity="0" class="fade-in-text">
         P(unripe) * P(green-black | unripe) * P(soft | unripe) = 17/51 * 7/17 * 1/17 = 0.008
    </text>
    </svg>

    <svg id=titText width="1000" height="200" xmlns="http://www.w3.org/2000/svg">
    <!-- Define the text element -->
    <text x="360" y="55" text-anchor="middle" alignment-baseline="middle" font-family="Arial" font-size="20" fill="black">
         P(unripe | green-black ∩ soft) ∝ 
    </text>
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
    margin-right: 10px; /* Add right margin to create space between images */
    margin-left: 100px;
    display: inline-block;
  }
  .image2 {
    margin-right: 100px; /* Add right margin to create space between images */
    margin-left: 1px;
    display: inline-block;
  }
  .image3 {
    margin-right: 100px; /* Add right margin to create space between images */
    margin-left: 450px;
    display: inline-block;
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
    opacity: 0; /* Initially set opacity to 0 */
    animation: fadeIn 10s forwards; /* Apply fadeIn animation */
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


#svgContainer {
  display: inline-block;
  margin-left: 0px; /* Adjust the value as needed */
  margin-top: -15px;
 
}
#svgContainer2 {
  display: inline-block;
  position: absolute;
  left: 720px; /* Adjust the horizontal position */
  top: 220px; /* Adjust the vertical position */

}
#svgContainer3 {
  margin-left: 450px; /* Adjust the value as needed */
  margin-top: 171px;
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

    @keyframes strikethroughAnimation {
        from {
            stroke-dashoffset: 100%; /* Start with full length */
            opacity: 0; /* Start with opacity 0 */
        }
        to {
            stroke-dashoffset: 0%; /* End with no length */
            opacity: 1; /* End with opacity 1 */
        }
    }

    .animated-strikethrough {
        animation: strikethroughAnimation 5s forwards;
        stroke-dasharray: 100%; /* Initial length */
        stroke-dashoffset: 0%; /* Start with full length */
        opacity: 0; /* Start with opacity 0 */
        animation-delay: 1.5s;
    }

    @keyframes fadeInText {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

.fade-in-text {
  animation: fadeInText 4s ease-in forwards; /* Adjust the duration and timing function as needed */
  animation-delay: 1.5s; /* Wait for 2 seconds before starting */
}

#corrText {
  display: inline-block;
  position: absolute;
  left: 720px; /* Adjust the horizontal position */
  top: 280px; /* Adjust the vertical position */
}

#titText {
  display: inline-block;
  position: absolute;
  left: 700px; /* Adjust the horizontal position */
  top: 170px; /* Adjust the vertical position */
}

</style>
