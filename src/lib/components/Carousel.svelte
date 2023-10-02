<script>
  import { fly } from "svelte/transition";
  import { cats } from "$lib/ktities";
  const noGroups = cats.slice(2);
</script>

<section
  transition:fly={{ y: 100, duration: 2000, opacity: 0, delay: 1000 }}
  class="mt-4 carousel carousel-center carousel-vertical h-[20rem] rounded-box bg-neutral p-2 shadow-md">
  {#each noGroups as image}
    <div class="mt-4 carousel-item h-full">
      <img src={image} alt="A kitten!" class="rounded-box" />
    </div>
  {/each}
</section>

<style>
  img {
    @apply shadow-md;
  }
</style>
