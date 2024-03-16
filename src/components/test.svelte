<!-- LargeBlueCircle.svelte -->
<script>
  import { onMount } from "svelte";
  import { writable } from "svelte/store";
  import "katex/dist/katex.min.css";
  import equation from "$lib/assets/equation.png";
  import multiply from "$lib/assets/multiply.png";
  import pA from "$lib/assets/P(A).png";
  import pB from "$lib/assets/P(B).png";
  import pBGA from "$lib/assets/P(B_A).png";
  import pAGB from "$lib/assets/P(A_B).png";

  let circleA, circleB, intersection, h1, p;

  // Define writable stores for h1 and p content
  const h1Content = writable("Bayes Theorem");
  const pContent = writable("Let's say we're rolling a dice🎲. Try hovering over the formula or the circles to further understand.");

  // Function to update h1 content
  function setH1Content(content) {
    h1Content.set(content);
  }

  // Function to update p content
  function setPContent(content) {
    pContent.set(content);
  }

  onMount(() => {
    const circleA = document.getElementById("circleA");
    const circleB = document.getElementById("circleB");
    const intersection = document.getElementById("intersection");

    const pA = document.getElementById("A");
    const pB = document.getElementById("B");
    const pBGA = document.getElementById("BGA");

    const h1 = document.querySelector("h1");
    const p = document.querySelector("p");

    circleA.addEventListener("mouseover", () => highlight("circleA"));
    circleB.addEventListener("mouseover", () => highlight("circleB"));
    intersection.addEventListener("mouseover", () => highlight("intersection"));

    circleA.addEventListener("mouseout", () => removeHighlight("circleA"));
    circleB.addEventListener("mouseout", () => removeHighlight("circleB"));
    intersection.addEventListener("mouseout", () =>
      removeHighlight("intersection"),
    );

    pA.addEventListener("mouseover", () => highlight("circleA"));
    pB.addEventListener("mouseover", () => highlight("circleB"));
    pBGA.addEventListener("mouseover", () => highlight("intersection"));

    pA.addEventListener("mouseout", () => removeHighlight("circleA"));
    pB.addEventListener("mouseout", () => removeHighlight("circleB"));
    pBGA.addEventListener("mouseout", () => removeHighlight("intersection"));
  });

  function highlight(elementId) {
    document.getElementById(elementId).classList.add("highlighted");
    // Update h1 and p tags
    switch (elementId) {
      case "circleA":
        document.getElementById("circleA").style.fill = "rgb(100, 153, 209)";
        document.getElementById("intersection").style.fill =
          "rgb(100, 153, 209)";
        setH1Content("P(A): Probability of A");
        setPContent(
          "Circle A indicated an outcome. For example, we can say that A is the event that our dice is an even number.",
        );
        break;
      case "circleB":
        document.getElementById("circleB").style.fill = "rgb(209, 185, 100)";
        document.getElementById("intersection").style.fill = "rgb(209, 185, 100)";
        setH1Content("P(B): Probability of B");
        setPContent(
          "Similarly, we can label another arbitrary outcome of the event as B, which could be the event that the dice is less than 3.",
        );
        break;
      case "intersection":
      document.getElementById("intersection").style.fill = "rgb(64, 158, 64)";
        setH1Content("P(B|A): Probability of B given A = P(A ∩ B): Probability of A and B");
        setPContent(
          "In the overlapping section A and B are simultaneously occuring. If we rolled a dice, the event that the number is both even and less than 3 is 2.",
        );
        break;
      default:
        break;
    }
  }

  function removeHighlight(elementId) {
    document.getElementById(elementId).classList.remove("highlighted");
    // Restore original content of h1 and p tags
    document.getElementById("circleA").style.fill = "#d8dadc";
    document.getElementById("circleB").style.fill = "#d8dadc";
    document.getElementById("intersection").style.fill = "#9fa3a6";
    setH1Content("Bayes Theorem");
    setPContent("Let's say we're rolling a dice🎲. Try hovering over the formula or the circles to further understand.");
  }
</script>

<main>
  <h1>{$h1Content}</h1>
  <p>{$pContent}</p>
    <svg width="1000" height="500">
      <!-- Circle A -->
      <circle
        id="circleA"
        cx="400"
        cy="250"
        r="200"
        class="circle"
        onmouseover="highlight('circleA')"
        onmouseout="removeHighlight('circleA')"
      >
        <text x="400" y="250" text-anchor="middle" alignment-baseline="middle"
          >A</text
        >
        <title>Probability space for event A</title>
      </circle>

      <!-- Circle B -->
      <circle
        id="circleB"
        cx="600"
        cy="250"
        r="200"
        class="circle"
        onmouseover="highlight('circleB')"
        onmouseout="removeHighlight('circleB')"
      >
        <text x="600" y="250" text-anchor="middle" alignment-baseline="middle"
          >B</text
        >
        <title>Probability of B</title>
      </circle>

      <!-- Intersection -->
      <path
        d="M500,423.2 A200,200, 0 0 1,500,76.759 A200,200, 0 0 0,500,76.759 A200,200, 0 0 1,500,423.2"
        id="intersection"
        class="intersection circle"
        onmouseover="highlight('intersection')"
        onmouseout="removeHighlight('intersection')"
      >
        <text x="600" y="250" text-anchor="middle" alignment-baseline="middle"
          >A ∩ B</text
        >
        <title>Probability of A and B</title>
      </path>
    </svg>
    <img
      id="A"
      src={pA}
      alt="P(A)"
      onmouseover="highlight('circleA')"
      onmouseout="removeHighlight('circleA')"
    />
    <img
      id="B"
      src={pB}
      alt="P(B)"
      onmouseover="highlight('circleB')"
      onmouseout="removeHighlight('circleB')"
    />
    <img
      id="BGA"
      src={pBGA}
      alt="P(B|A)"
      onmouseover="highlight('intersection')"
      onmouseout="removeHighlight('intersection')"
    />
    <img id="AGB" src={pAGB} alt="P(A|B)" />
    <img id="equation" src={equation} alt="= /" />
    <img id="multiply" src={multiply} alt="*" />

    <!-- SVG for BG -->
    <svg id="svgContainer3" width="400" height="100" xmlns="http://www.w3.org/2000/svg">
    <!-- Create a rectangle -->
    <rect width="200" height="50" x="1" y="25" fill="none" stroke=none stroke-width="2" />

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
    height: 100%;
    width: 100%;
    background-color: beige;
    margin: 0;
    padding: 0;
  }
  .circle {
    fill: #d8dadc;
    stroke: black;
    transition: fill 0.3s ease;
  }
  .intersection {
    fill: #9fa3a6;
    stroke: black;
    transition: fill 0.3s ease;
  }

  .highlighted {
    fill: #6cb4ee !important;
  }
  img {
    mix-blend-mode: multiply;
  }
  #A {
    width: 64px;
    position: absolute;
    top: 280px;
    left: 1150px;
  }
  #B {
    width: 64px;
    position: absolute;
    top: 340px;
    left: 1095px;
  }
  #BGA {
    width: 90px;
    position: absolute;
    top: 280px;
    left: 1035px;
  }
  #AGB {
    width: 90px;
    position: absolute;
    top: 310px;
    left: 890px;
  }
  #equation {
    width: 240px;
    position: absolute;
    top: 320px;
    left: 990px;
  }
  #multiply {
    width: 15px;
    position: absolute;
    top: 280px;
    left: 1130px;
  }
  #svgContainer3 {
  margin-left: 510px; /* Adjust the value as needed */
  margin-top: 160px;
  }
</style>
