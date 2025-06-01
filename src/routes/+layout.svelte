<script>
  import "@fontsource-variable/dm-sans";
  import "../app.css";

  let { children } = $props();
</script>

{@render children()}

<style>
  :global(body) {
    font-family: "DM Sans Variable", sans-serif;
  }
</style>
