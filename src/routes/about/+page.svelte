<script>
	import alinaheadshot from '$lib/images/alinaheadshot.jpg';
</script>

<svelte:head>
	<title>About</title>
	<meta name="description" content="About Alina" />
</svelte:head>

<section>
	<h1>About Alina</h1>
	<span class="heading-photo">
        <img src={alinaheadshot} alt="Alina" />
    </span>
</section>

<style>
    img {
        max-width: 20em;
    }
</style>