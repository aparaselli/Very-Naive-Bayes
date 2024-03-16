<!-- LargeBlueCircle.svelte -->
<script>
  // You can define any additional logic here if needed
  const videoUrl = 'https://www.youtube.com/embed/W_0_tD0sZWs&ab_channel';
</script>

<main>
  <h1>Predicting The Unknown Using <s>Magic</s> Math</h1>
  <p> An explanation of how simple math and observation can be coupled to use the naive bayes classification technique to make predictions </p>
    <div class="video-container">
    <iframe
      width=50%
      height=100%
      
      src="https://www.youtube.com/embed/W_0_tD0sZWs"
      alt='demo video'
      title="Why Use Our Naive Bayes Website?"
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

    margin: 0;
    padding: 0;
  }

  .video-container {
    position: absolute; /* Change to absolute positioning */
    width: 1000px;
    height: 300px;
    top: 50%; /* Position it 50% from the top */
    left: 50%; /* Position it 50% from the left */
    transform: translate(-50%, -50%); /* Center the element */
  }
  iframe {
  display:block;
  margin:auto;
}

</style>
