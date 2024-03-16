<!-- App.svelte -->
<script>
  import Page0 from './Hook.svelte';
  import Page1 from './ProbA.svelte';
  import Page2 from './ProbB.svelte';
  import Page3 from './ProbAB.svelte';
  import Page4 from './ProbBGA.svelte';
  import Page5 from './test.svelte';
  import Page6 from './ripe_unripe.svelte';
  import Page7 from './with_one_col.svelte';
  import Page8 from './CondIndep.svelte';
  import Page9 from './with_two_col.svelte';
  import Page10 from './CreatingAModel.svelte';
  import Page11 from './SmoothingAModel.svelte';
  import Page12 from './TrainingAModel.svelte';
  import Page13 from './Conclusion.svelte';
  

  import Layout from './Layout.svelte';

  let currentVisualization = Page0; // Initial visualization is Page1

  function switchVisualization(page) {
    switch (page) {

      case 'Page0.svelte':
        currentVisualization = Page0;
        break;
      case 'Page1.svelte':
        currentVisualization = Page1;
        break;
      case 'Page2.svelte':
        currentVisualization = Page2;
        break;
      case 'Page3.svelte':
        currentVisualization = Page3;
        break;
      case 'Page4.svelte':
        currentVisualization = Page4;
        break;
      case 'Page5.svelte':
        currentVisualization = Page5;
        break;
      case 'Page6.svelte':
        currentVisualization = Page6;
        break;
      case 'Page7.svelte':
        currentVisualization = Page7;
        break;
      case 'Page8.svelte':
        currentVisualization = Page8;
        break;
      case 'Page9.svelte':
        currentVisualization = Page9;
        break;
      case 'Page10.svelte':
        currentVisualization = Page10;
        break;
      case 'Page11.svelte':
        currentVisualization = Page11;
        break;
      case 'Page12.svelte':
        currentVisualization = Page12;
        break;
      case 'Page13.svelte':
        currentVisualization = Page13;
        break;
      default:
        break;
    }
  }
</script>

<Layout {currentVisualization} {switchVisualization} />
