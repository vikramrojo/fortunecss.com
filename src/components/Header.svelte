<script>
  import Nav from "./Nav.svelte";

  export let segment;
</script>

<style>

</style>

<header class="marB3">
  <nav class="nav cols">
    <div class="col3 hide">
      <img src="logo.svg" class="ht2" />
      Fortune.css
    </div>
    <div class="navLeft col">
      <a class={segment === undefined ? 'bold bgLight' : ''} href=".">home</a>
      <a
        class={segment === 'docs' ? 'bold bgLight' : ''}
        href="docs/components">
        docs
      </a>
      <a class={segment === 'about' ? 'bold bgLight' : ''} href="about">
        about
      </a>
    </div>
    <div class="navRight col" />
  </nav>
</header>
