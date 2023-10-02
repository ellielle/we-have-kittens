<script lang="ts">
  import { onMount } from "svelte";
  // @ts-ignore # Cannot find module error
  import CatInfo from "$lib/components/CatInfo.svelte";
  import Carousel from "$lib/components/Carousel.svelte";
  import { cats } from "$lib/ktities";
  import { fly } from "svelte/transition";
  import "../app.css";
  import Modal from "$lib/components/Modal.svelte";
  let loaded = false;
  let showModal = false;
  let image: string | null = null;

  function handleKitten(event: CustomEvent) {
    showModal = true;
    image = event.detail;
  }

  onMount(() => {
    loaded = true;
  });
</script>

<main
  data-theme="dark"
  class="flex flex-col place-items-center place-content-center mx-auto max-w-[1280px] bg-base-300">
  {#if loaded}
    <h1 transition:fly={{ y: 50, duration: 2000, opacity: 0 }} class="mt-8 text-3xl text-center">
      The Quality Lab has kittens!
    </h1>

    <CatInfo />

    <div
      class="card-compact bg-base-200 rounded-box shadow-md"
      transition:fly={{ y: 50, duration: 1000, opacity: 0, delay: 400 }}>
      <div
        transition:fly={{ y: 50, duration: 2000, opacity: 0, delay: 400 }}
        class="card-body mt-4">
        <img src={cats[0]} alt="A bunch of kittens!" class="rounded-box shadow-md" />

        <img
          src={cats[1]}
          alt="A bunch of kittens!"
          class="rounded-box shadow-md mt-4"
          transition:fly={{ y: 50, duration: 2000, opacity: 0, delay: 400 }} />
      </div>
    </div>

    <p
      class="text-center text-orange-200 my-4"
      transition:fly={{ y: 50, duration: 2000, opacity: 0, delay: 600 }}>
      Swipe down for more pictures!
    </p>

    <Carousel on:kitten={handleKitten} />
    {#if image && showModal}
      <Modal bind:showModal>
        <img src={image} alt="A close-up kitten!" width="100%"/>
      </Modal>
    {/if}
  {/if}
  <div class="mt-8 divider">
    <p class="text-sm">Made with 🐈❤️</p>
  </div>
</main>
