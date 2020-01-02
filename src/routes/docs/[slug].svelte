<script context="module">
  export async function preload({ params, query }) {
    // the `slug` parameter is available because
    // this file is called [slug].html
    const res = await this.fetch(`docs/${params.slug}.json`);
    const data = await res.json();

    if (res.status === 200) {
      return { post: data };
    } else {
      this.error(res.status, data.message);
    }
  }
</script>

<script>
  import Bio from "../../components/Bio.svelte";
  export let post;
</script>

<style>

</style>

<svelte:head>
  <title>{post.title}</title>
</svelte:head>

<header>
  <h1>{post.title}</h1>
</header>
<div class="container">
  <article class="content">
    {@html post.html}
  </article>
  <hr />
  <small>{post.printDate} ~ {post.printReadingTime}</small>
  <Bio />
</div>
