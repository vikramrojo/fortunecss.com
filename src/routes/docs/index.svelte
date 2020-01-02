<script context="module">
  export function preload({ params, query }) {
    return this.fetch(`docs.json`)
      .then(r => r.json())
      .then(posts => {
        return { posts };
      });
  }
</script>

<script>
  export let posts;
  export let segment;
</script>

<style>

</style>

<svelte:head>
  <title>Docs</title>
</svelte:head>

<ul>
  {#each posts as post, index}
    <li class="post-item">
      <a rel="prefetch" href="docs/{post.slug}">{post.title}</a>
    </li>
  {/each}
</ul>
