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

<section class="cols">
  <article class="col2">
    <ul>
      <li class={segment === undefined ? 'bold' : ''}>
        <a href="/docs">Introduction</a>
      </li>
      {#each posts as post, index}
        <li class="post-item">
          <a rel="prefetch" href="docs/{post.slug}">{post.title}</a>
        </li>
      {/each}
    </ul>
  </article>
  <article>
    <h2>Documentation</h2>
  </article>
</section>
