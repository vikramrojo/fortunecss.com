<script>
  import Header from "../components/Header.svelte";

  export let segment;
</script>

<style>

</style>

<div class="viewHt100 flex flexCol flexBetween">
  <Header {segment} />

  <main class="padY4">
    <slot />
  </main>

  <footer class="wid100">
    <nav class="nav cols">
      <div class="navLeft col">
        <a href="https://github.com/atav1k/sapper-fortune-template">Github</a>
        <a href="/">&copy; {new Date().getFullYear()}</a>
      </div>
    </nav>
  </footer>
</div>
