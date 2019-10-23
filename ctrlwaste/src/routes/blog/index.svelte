<script context="module">
	export function preload({ params, query }) {
		return this.fetch(`blog.json`).then(r => r.json()).then(posts => {
			return { posts };
		});
	}
</script>

<script>
	export let posts;
</script>

<style>
	ul {
		margin: 0 0 1em 0;
		line-height: 1.5;
	}
</style>

<svelte:head>
	<title>Tools</title>
</svelte:head>

<h1>Open-Source Software</h1>
<ul>
  <li><a rel='prefetch' target="_blank" href='https://github.com/MPH-Bali/green-village-project'>Green Village Project</a></li>
  <li><a rel='prefetch' target="_blank" href='https://github.com/mjday/trashbounty'>Trash Bounty</a></li>
</ul>

<!-- <h1>Stories</h1>
<ul>
	{#each posts as post}
		we're using the non-standard `rel=prefetch` attribute to
				tell Sapper to load the data for the page as soon as
				the user hovers over the link or taps it, instead of
				waiting for the 'click' event
		<li><a rel='prefetch' href='blog/{post.slug}'>{post.title}</a></li>
	{/each}
</ul>
 -->
