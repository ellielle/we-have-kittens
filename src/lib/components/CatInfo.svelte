<script>
  import { fly } from "svelte/transition";
</script>

<section transition:fly={{ y: 100, duration: 2000, opacity: 0, delay: 200 }}>
  <!-- svelte-ignore a11y-no-noninteractive-tabindex -->
  <div tabindex="0" class="collapse collapse-arrow text-center">
    <div class="collapse-title text-xl px-0">More Information</div>
    <div class="collapse-content">
      <ul>
        <li class="text-orange-200">
          <p>Mom has her shots and tested negative on her FeLV(leukemia)/FIV SNAP test.</p>
        </li>
        <li class="mt-2">
          <p>
            Only the white, orange tabby, and tuxedo kittens are available. All 3 of them are boys.
          </p>
        </li>
        <li class="mt-2">
          <p>
            🎉 They were born on September 4th and will be ready to be re-homed starting October 23rd. 🎉
          </p>
        </li>
      </ul>
    </div>
  </div>
</section>

<style>
  li {
    list-style: disc;
  }
</style>
