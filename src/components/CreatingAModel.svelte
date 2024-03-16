<!-- LargeBlueCircle.svelte -->
<script>
    import Icon from "$lib/assets/iconNoBG.png";
    import Arrow from "$lib/assets/arrow.png";
    import Cog from "$lib/assets/cog.png";
  // You can define any additional logic here if needed
     
</script>

<main>
  <h1>Creating a Model</h1>

  <p>
    Now that we know how to make a prediction on an avacodo, we may realize that writing out all these computations by hand can be exhausting. Especially if we start predicting on a lot of features!
    Therefore we will use a computer and some code to create a model. A model is a object we input data into 
    and it outputs a classification. In our case we would input data about an avocado and it would output whether the avocado was ripe or not.
  </p>

  <img
      id="A"
      src={Icon}
      class = "image"

    />
    <img
      id="B"
      src={Arrow}
      class = "image2"
    />
    <img
      id="B"
      src={Arrow}
      class = "image3"
    />


    <svg id="svgContainer" width="1000" height="450">
    <image href={Cog} width="100" height="100" x="650" y="10" />
     <g id="allShapes">
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

        <polygon class="greenblack-soft" points="540, 108 550, 91 560, 108"
        ></polygon>
        <polygon class="greenblack" points="540, 158 550, 141 560, 158"></polygon>
        <polygon class="greenblack" points="540, 208 550, 191 560, 208"></polygon>
        <polygon class="greenblack" points="540, 258 550, 241 560, 258"></polygon>

        <polygon class="soft" points="590, 108 600, 91 610, 108"></polygon>
        <polygon points="590, 158 600, 141 610, 158"></polygon>
        <polygon points="590, 208 600, 191 610, 208"></polygon>
        <polygon points="590, 258 600, 241 610, 258"></polygon>

        <polygon points="640, 108 650, 91 660, 108"></polygon>
        <polygon points="640, 158 650, 141 660, 158"></polygon>
        <polygon points="640, 208 650, 191 660, 208"></polygon>
        <polygon points="640, 258 650, 241 660, 258"></polygon>
        </g>
      </g>
      <rect x="175" y="70" width="510" height="215" fill="none" stroke="black" stroke-width="2" />
    </svg>

    <!-- SVG for BG -->
    <svg id="svgContainer3" width="400" height="100" xmlns="http://www.w3.org/2000/svg">
    <!-- Create a rectangle -->
    <rect width="200" height="50" x="1" y="25" fill=none stroke=none stroke-width="2" />

    <!-- Add text inside the rectangle -->
    <text x="100" y="55" text-anchor="middle" alignment-baseline="middle" font-family="Arial" font-size="20" fill="black"> </text>
    </svg>

    <!-- SVG for Label -->
    <svg id="svgContainer2" width="300" height="100" xmlns="http://www.w3.org/2000/svg">
    <!-- Create a rectangle -->
    <rect width="200" height="50" x="1" y="25" fill="lightblue" stroke="black" stroke-width="2" />

    <!-- Add text inside the rectangle -->
    <text x="100" y="55" text-anchor="middle" alignment-baseline="middle" font-family="Arial" font-size="20" fill="black">This Avocado is Ripe!</text>
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
    margin-left: 180px;
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



#svgContainer {
  display: inline-block;
  margin-left: 530px; /* Adjust the value as needed */
  margin-top: -375px;
 
}
#svgContainer2 {
  display: inline-block;
  position: absolute;
  left: 1480px; /* Adjust the horizontal position */
  top: 305px; /* Adjust the vertical position */

}
#svgContainer3 {
  margin-left: 450px; /* Adjust the value as needed */
  margin-top: 155px;
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




</style>
