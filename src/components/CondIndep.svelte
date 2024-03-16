<script>
  // You can define any additional logic here if needed
  import heads from "$lib/assets/coin_heads.png";
  import tails from "$lib/assets/coin_tails.png";
</script>

<main>
  <h1>But what if we wanted to predict on more features?</h1>

  <p>
    Let say we also knew the softness of Avi! Now, when predicting ripeness
    using color and softness, we narrow our search to avocados with matching
    color and softness. However, this approach poses a problem as it ignores
    variations in the bag of avocados (dataset).
  </p>
  <p>
    If we know Avi is green-black AND soft, we would
    only look at the green circles, which would force us to ignore all the blue
    and yellow points. To ensure we extract value from a broader range of
    avocados (and lower computations), we make the simplifying assumption that
    our features are independent given ripeness.
  </p>
  <p>
    In essence, once we know an avocado's ripeness, color no longer affects
    softness and vice versa. This principle is known as conditional
    independence.
  </p>

  <svg width="1000" height="360">
    <g id="ripe">
      <text class="label" x="250" y="50">P(ripe) = 24 / 50</text>
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
      <text class="label" x="500" y="50">P(unripe) = 16 / 50</text>
      <text x="40" y="63.5" transform="rotate(270, 40, 120) scale(2,11)">}</text
      >
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
    <!-- Legend -->
    <rect x="190" y="300" width="40" height="10" fill="#6cb4ee" />
    <text x="240" y="310" font-family="Arial">Green-Black</text>
    <rect x="190" y="320" width="40" height="10" fill="#f0e68c" />
    <text x="240" y="330" font-family="Arial">Soft</text>
    <rect x="190" y="340" width="40" height="10" fill="#6deb86" />
    <text x="240" y="350" font-family="Arial">Green-Black & Soft</text>
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
    margin-top: 0.5%;
    margin-bottom: 0%;
    padding-left: 188px;
    padding-right: 188px;
    font-family: Arial, Helvetica, sans-serif;
    font-size: 18px; /* Increase font size */
    line-height: 1.5; /* Double-spaced text */
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

  circle {
    fill: None;
    stroke: black;
  }

  .label {
    font-size: 18px;
    font-family: Arial;
  }
</style>
