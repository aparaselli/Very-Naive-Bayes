<!-- LargeBlueCircle.svelte -->
<script>
  import Icon from "$lib/assets/iconNoBG.png";
  import Arrow from "$lib/assets/arrow.png";
  import Model from "$lib/assets/trainedmodel.png";

  // You can define any additional logic here if needed
</script>

<main>
  <h1>Conclusion And Takeaways</h1>

  <p>
    Now that we have a model we can make predictions about Avi and all of
    friends with ease! We hope that through the use of our animations, examples
    and emphasis on visuals to represent data you were able to successfully
    understand the basics and most importantly, the inuition behind the Naive
    Bayes classifier. You now know basic probility rules, the math used to make
    a prediction, and the methodology behind creating a naive bayes
    classification model. Using this knowledge your ready to tackle
    classification problems and learn more about the world of machine learning!
  </p>

  <img alt="avocado" id="A" src={Icon} />
  <img alt="avocado" class="image" src={Icon} />
  <img alt="avocado" class="image" src={Icon} />

  <img id="B" src={Arrow} class="image3" alt="arrow" />

  <img id="model" src={Model} alt="trained model" />
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
  #A {
    width: 100px;
    margin-left: 12%;
    padding-bottom: 2%;
  }
  .image {
    width: 100px;
   padding-bottom: 2%;
  }
  .image3 {
    width: 100px;
    display: inline-block;
    position: relative;
    margin-bottom: 5%;
   
  }

  #model {
    padding-top: 2%;
    width: 35%;
  }
  @keyframes fadeIn {
    from {
      opacity: 0; /* Start with opacity 0 */
    }
    to {
      opacity: 1; /* End with opacity 1 */
    }
  }

  @keyframes rotate {
    from {
      transform: rotate(0deg); /* Start rotation from 0 degrees */
    }
    to {
      transform: rotate(360deg); /* End rotation at 360 degrees */
    }
  }
</style>
