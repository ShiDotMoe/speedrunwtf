<script context="module">
  const games = [
    {
      title: 'Super Mario 64',
      slug: 'sm64',
      cover: '../covers/sm64.png',
      categories: 1,
      runners: 0
    }
  ];
</script>

<style>
	article {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
  }
  
  img {
    width: 160px;
    border-radius: .5rem;
  }
</style>

<svelte:head>
	<title>Games - speedrun.wtf</title>
</svelte:head>

<h1>Games</h1>

<section>
	{#each games as game}
		<article>
      <a rel="prefetch" href="games/{game.slug}">
        <img src={game.cover} alt={game.title}/>
        <h2>{game.title}</h2>
      </a>
      <span>{game.categories} category</span>
      <span>{game.runners} runners</span>
    </article>
	{/each}
</section>