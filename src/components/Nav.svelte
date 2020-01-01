<script>
  export let segment;
</script>

<style>

</style>

<nav class="nav cols">
  <div class="col navLeft">
    <a class={segment === undefined ? 'bold' : ''} href=".">home</a>
    <a class={segment === 'about' ? 'bold' : ''} href="about">about</a>
    <a rel="prefetch" class={segment === 'blog' ? 'bold' : ''} href="blog">
      blog
    </a>
  </div>
</nav>
