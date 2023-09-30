<script>
  import { onMount } from "svelte";
  // @ts-ignore # Cannot find module error
  import { Meow1, Meow2, Meow3 } from "$lib/ktities";
  import { fly } from "svelte/transition";
  import "../app.css";
  let loaded = false;

  onMount(() => {
    loaded = true;
  });
</script>

<main class="flex flex-col place-items-center">
  {#if loaded}
    <h1 transition:fly={{ y: 100, duration: 2000, opacity: 0 }} class="mt-8 text-3xl text-center">
      We have kittens!
    </h1>
  {/if}

  {#if loaded}
    <div transition:fly={{ y: 100, duration: 2000, opacity: 0, delay: 300 }} class="mt-4">
      <img src={Meow1} alt="A bunch of kittens!" class="rounded-box" />
    </div>
  {/if}

  {#if loaded}
    <div transition:fly={{ y: 100, duration: 2000, opacity: 0, delay: 700 }} class="mt-4">
      <img src={Meow2} alt="A bunch of kittens!" class="rounded-box" />
    </div>
  {/if}

  {#if loaded}
    <div transition:fly={{ y: 100, duration: 2000, opacity: 0, delay: 1200 }} class="mt-4">
      <img src={Meow3} alt="A bunch of kittens!" class="rounded-box" />
    </div>
  {/if}
</main>
