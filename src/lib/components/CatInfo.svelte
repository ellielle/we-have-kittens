<script>
  import { fly } from "svelte/transition";
</script>

<section transition:fly={{ y: 100, duration: 2000, opacity: 0, delay: 200 }}>
  <!-- svelte-ignore a11y-no-noninteractive-tabindex -->
  <div tabindex="0" class="collapse">
    <div class="collapse-title text-xl text-center">More Information</div>
    <div class="collapse-content">
      <ul>
        <li class="text-red-500">
          Mom has her shots and tested FIV & OTHER NASTY DISEASES Negative
        </li>
        <li>Only the white, orange tabby, and tuxedo kittens are available. All 3 are male.</li>
      </ul>
    </div>
  </div>
</section>
