<script>
  import { fly } from "svelte/transition";
</script>

<section>
  <details class="shadow-lg" transition:fly={{ y: 100, duration: 2000, opacity: 0, delay: 200 }}>
    <summary> Mom's Health Information:</summary>
    <ul>
      <li>FIV Negative</li>
      <li>Negative</li>
      <li>Has Shots</li>
      <li>Smokes Weed</li>
      <li>Does Crime</li>
    </ul>
  </details>
</section>

<style>
  @keyframes details-show {
    from {
      opacity: 0;
      transform: var(--details-translate, translateY(-0.5em));
    }
  }

  details[open] > *:not(summary) {
    animation: details-show 150ms ease-in-out;
  }
</style>
