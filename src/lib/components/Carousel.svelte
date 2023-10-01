<script>
  import { fly } from "svelte/transition";
  import { Dragon, Dragon2, Tux, Tux2, Orange, Orange2 } from "$lib/ktities";
</script>

<section
  transition:fly={{ y: 100, duration: 2000, opacity: 0, delay: 1000 }}
  class="mt-4 carousel carousel-vertical h-[20rem] rounded-box bg-base-200 p-2 shadow-md"
>
  <div class="mt-4 carousel-item h-full">
    <img src={Dragon} alt="A bunch of kittens!" class="rounded-box" />
  </div>
  <div class="mt-4 carousel-item h-full">
    <img src={Dragon2} alt="A bunch of kittens!" class="rounded-box" />
  </div>
  <div class="mt-4 carousel-item h-full">
    <img src={Tux} alt="A bunch of kittens!" class="rounded-box" />
  </div>
  <div class="mt-4 carousel-item h-full">
    <img src={Tux2} alt="A bunch of kittens!" class="rounded-box" />
  </div>
  <div class="mt-4 carousel-item h-full">
    <img src={Orange} alt="A bunch of kittens!" class="rounded-box" />
  </div>
  <div class="mt-4 carousel-item h-full">
    <img src={Orange2} alt="A bunch of kittens!" class="rounded-box" />
  </div>
</section>

<style>
  img {
    @apply shadow-md;
  }
</style>
