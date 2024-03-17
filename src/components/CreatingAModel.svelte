<!-- LargeBlueCircle.svelte -->
<script>
  import Icon from "$lib/assets/iconNoBG.png";
  import Arrow from "$lib/assets/arrow.png";
  import Model from "$lib/assets/model.png";
  // You can define any additional logic here if needed
</script>

<main>
  <h1>Creating a Model</h1>

  <p>
    Now that we know how to make a prediction on an avacodo, we may realize that
    writing out all these computations by hand can be exhausting. Especially if
    we start predicting on a lot of features! Therefore we will use a computer
    and some code to create a model. A model is a object we input data into and
    it outputs a classification. In our case we would input data about an
    avocado and it would output whether the avocado was ripe or not.
  </p>
  <img alt="avocado" id="A" src={Icon}  />
  <img alt="arrow" src={Arrow} class="image2" />
  <img alt="model" src={Model} class="model" />
  <img alt="arrow" src={Arrow} class="image2" />
  <!-- SVG for Label -->
  <svg
    id="svgContainer2"
    width="200"
    height="100"
    xmlns="http://www.w3.org/2000/svg"
  >
    <text
      x="100"
      y="55"
      text-anchor="middle"
      alignment-baseline="middle"
      font-family="Arial"
      font-size="20"
      fill="black">This Avocado is Ripe!</text
    >
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

  .image2 {
    width: 100px;
    margin-bottom: 2%;
  }
  #A {
    margin-left: 188px;
    width: 100px; /* Set the width to the desired smaller size */
    height: auto; /* Maintain aspect ratio */
  }
  #svgContainer2 {
    position: relative;
    padding-left: 1%;
    padding-bottom: 1%;
  }
 .model {
  padding-left: 20px;
  width: 30%;
 }
</style>
