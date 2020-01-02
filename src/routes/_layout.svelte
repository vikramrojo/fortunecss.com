<script>
  import Header from "../components/Header.svelte";
  import Nav from "../components/Nav.svelte";

  export let segment;
</script>

<style>

</style>

<div class="viewHt100">
  <Header {segment} />

  <main class="cols">
    <Nav {segment} />
    <article class="col">
      <slot />
    </article>
  </main>

  <footer class="wid100">
    <nav class="nav cols">
      <div class="navLeft col">&copy; {new Date().getFullYear()}</div>
    </nav>
  </footer>
</div>
