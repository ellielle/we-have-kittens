<script>
  import { dev } from "$app/environment";
  import { inject } from "@vercel/analytics";

  inject({ mode: dev ? "development" : "production" });
</script>

<slot />

<style>
  :global(body) {
    @apply bg-base-300;
  }
</style>
