<script>
  import Icon from "$lib/assets/icon.jpg";
  import { onMount } from "svelte";
  // Function to set the transform attribute value to move the <g> element
    onMount(() => {
    // Move unripe after 2 seconds
    let elem = document.getElementById("unripe");
    elem.style.opacity = "1";
    setTimeout(() => {
        elem.style.opacity = "0"; // Fade in
      }, 1000);
    setTimeout(() => {
      elem.setAttribute("transform", "translate(300, 0)");
      elem.style.transition = "transform 1s ease-in-out, opacity 1s ease-in-out";
      elem.style.opacity = "1"; 
      // Create SVG text element
      const svg1 = document.getElementById("ripe");
      const text1 = document.createElementNS(
        "http://www.w3.org/2000/svg",
        "text",
      );
      text1.setAttribute("x", "500");
      text1.setAttribute("y", "100");
      text1.setAttribute("fill", "blue");
      text1.setAttribute("font-family", "Arial");
      text1.textContent = "P(green-black | ripe) = 6/24";
      svg1.appendChild(text1);

      const text12 = document.createElementNS(
        "http://www.w3.org/2000/svg",
        "text",
      );
      text12.setAttribute("x", "500");
      text12.setAttribute("y", "150");
      text12.setAttribute("fill", "blue");
      text12.setAttribute("font-family", "Arial");
      text12.textContent = "P(green-black | ripe) * P(ripe)";
      svg1.appendChild(text12);

      const text13 = document.createElementNS(
        "http://www.w3.org/2000/svg",
        "text",
      );
      text13.setAttribute("x", "500");
      text13.setAttribute("y", "180");
      text13.setAttribute("fill", "blue");
      text13.setAttribute("font-family", "Arial");
      text13.textContent = "= 6/24 * 24/50 = 6/50";
      svg1.appendChild(text13);

      const text14 = document.createElementNS(
        "http://www.w3.org/2000/svg",
        "text",
      );
      text14.setAttribute("x", "500");
      text14.setAttribute("y", "220");
      text14.setAttribute("fill", "red");
      text14.setAttribute("font-family", "Arial");
      text14.textContent = "P(ripe | green-black) ∝ 6/50";
      svg1.appendChild(text14);

      const svg2 = document.getElementById("unripe");
      const text2 = document.createElementNS(
        "http://www.w3.org/2000/svg",
        "text",
      );
      text2.setAttribute('style', 'white-space: pre;');
      text2.setAttribute("x", "690");
      text2.setAttribute("y", "100");
      text2.setAttribute("fill", "blue");
      text2.setAttribute("font-family", "Arial");
      text2.textContent = "P(green-black | unripe) = 8/16";
      svg2.appendChild(text2);

      const text21 = document.createElementNS(
        "http://www.w3.org/2000/svg",
        "text",
      );
      text21.setAttribute('style', 'white-space: pre;');
      text21.setAttribute("x", "690");
      text21.setAttribute("y", "150");
      text21.setAttribute("fill", "blue");
      text21.setAttribute("font-family", "Arial");
      text21.textContent = "P(green-black | ripe) * P(ripe)";
      svg2.appendChild(text21);

      const text22 = document.createElementNS(
        "http://www.w3.org/2000/svg",
        "text",
      );
      text22.setAttribute('style', 'white-space: pre;');
      text22.setAttribute("x", "690");
      text22.setAttribute("y", "180");
      text22.setAttribute("fill", "blue");
      text22.setAttribute("font-family", "Arial");
      text22.textContent = "= 8/16 * 16/50 = 8/50";
      svg2.appendChild(text22);

      const text23 = document.createElementNS(
        "http://www.w3.org/2000/svg",
        "text",
      );
      text23.setAttribute("x", "690");
      text23.setAttribute("y", "220");
      text23.setAttribute("fill", "red");
      text23.setAttribute("font-family", "Arial");
      text23.textContent = "P(unripe | green-black) ∝ 8/50";
      svg2.appendChild(text23);

      const text24 = document.createElementNS(
        "http://www.w3.org/2000/svg",
        "text",
      );
      text24.setAttribute("x", "690");
      text24.setAttribute("y", "260");
      text24.setAttribute("fill", "purple");
      text24.setAttribute("font-size", "25");
      text24.setAttribute("font-weight", "bold");
      text24.setAttribute("font-family", "Arial");
      text24.textContent = "AVI IS UNRIPE";
      svg2.appendChild(text24);
    }, 2000);
  });
</script>

<main>
  <h1>Classifying an Avocado</h1>
  <p>
    Avi <span><img src={Icon} alt="download icon"/></span> is <span id="extra">green-black</span>.  We'll
    highlight all the green-black avocados in our bag in blue. Let's compare the probability that Avi is ripe
    with the probability that Avi is unripe. <span id="note">NOTE! we focus on the numerators of P(ripe | green-black) 
      and P(unripe | green-black) since their denominators are the same. This allows us to make our comparison using proportionality (∝) rather than equality (=).</span>
    </p>
    

  <svg width="1400" height="400">
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

      <circle cx="300" cy="100" r="10"></circle>
      <circle cx="300" cy="150" r="10"></circle>
      <circle cx="300" cy="200" r="10"></circle>
      <circle cx="300" cy="250" r="10"></circle>

      <circle cx="350" cy="100" r="10"></circle>
      <circle cx="350" cy="150" r="10"></circle>
      <circle cx="350" cy="200" r="10"></circle>
      <circle cx="350" cy="250" r="10"></circle>

      <circle class="greenblack" cx="400" cy="100" r="10"></circle>
      <circle class="greenblack" cx="400" cy="150" r="10"></circle>
      <circle class="greenblack" cx="400" cy="200" r="10"></circle>
      <circle cx="400" cy="250" r="10"></circle>

      <circle class="greenblack" cx="450" cy="100" r="10"></circle>
      <circle class="greenblack" cx="450" cy="150" r="10"></circle>
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

      <polygon class="greenblack" points="540, 108 550, 91 560, 108"></polygon>
      <polygon class="greenblack" points="540, 158 550, 141 560, 158"></polygon>
      <polygon class="greenblack" points="540, 208 550, 191 560, 208"></polygon>
      <polygon class="greenblack" points="540, 258 550, 241 560, 258"></polygon>

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
    <rect x="190" y="300" width="40" height="10" fill="#6cb4ee" />
    <text x="240" y="310" font-family="Arial">Green-Black</text>
  </svg>
</main>

<style>
  h1 {
    margin-left: 188px;
    padding-top: 10px;
    margin-right: 188px;
    font-family: Arial, Helvetica, sans-serif;
  }
  p {
    margin-left: 188px;
    margin-right: 188px;
    font-family: Arial, Helvetica, sans-serif;
            font-size: 18px; /* Increase font size */
        line-height: 1.5; /* Double-spaced text */
  }
  img {
    width: 50px;
    mix-blend-mode: multiply;
  }
  .label {
    font-size: 18px;
    font-family: Arial;
  }
  circle {
    fill: None;
    stroke: black;
  }
  .greenblack {
    fill: #6cb4ee;
  }
  #extra {
    font-weight: bold;
  }
  #note {
    font-size: 10pt;
    color: rgb(103, 101, 101);
  }
  polygon {
    fill: None;
    stroke: black;
  }

  @keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
</style>
