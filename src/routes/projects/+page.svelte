<script>
	import ProjectItem from "./react-photo-gallery/+page.svelte";
	import ProjectNav from "./ProjectNav.svelte";
	import foragingfinds from "$lib/images/foragingfindsimg.png";
	import vifiimg from "$lib/images/vifiimg.png";
	import reactgallery from "$lib/images/reactgalleryphoto.jpg";
	import reduxgallery from "$lib/images/reduxmovies.png";
	import calculator from "$lib/images/calculatorimg.png";

</script>
<svelte:head>
	<title>Alina Trukhina's Projects</title>
	<meta name="description" content="Alina Trukhina's Projects" />
</svelte:head>

<section class="projectsImgs">
	<!-- <h4>Explore My Recent Projects</h4>
	<h5>Foragins Finds app is currently deployed - feel free to check out the link to the website.</h5> -->

	<div class="imgcard">
		<a href="/projects/foraging-finds">
			<img class="projectImg" src={foragingfinds} alt='foraging finds'>
    	</a>
	</div>
	<div class="imgcard">
		<a href="/projects/womens-health-directory-vifi">
			<img class="projectImg" src={vifiimg} alt="Vifi, a Women's Health app">
    	</a>
	</div>
	<div class="imgcard">
		<a href="/projects/react-photo-gallery">
			<!-- svelte-ignore a11y-img-redundant-alt -->
			<img class="projectImg" src={reactgallery} alt='react photo gallery'>
		</a>
	</div>
	<div class="imgcard">
		<a href="/projects/react-redux-movie-gallery">
			<img class="projectImg" src={reduxgallery} alt='redux movie gallery'>
		</a>
	</div>
	<div class="imgcard">
		<a href="/projects/server-side-calculator">
			<img class="projectImg" src={calculator} alt='server-side calculator'>
		</a>
	</div>
</section>

<style>

.projectsImgs {
	display: flex;
	flex-wrap: wrap;
}

.imgcard {
	display: inline-flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
	background-color: rgba(100, 148, 237, 0.494);
	border-radius: 5px;
	margin: 1em;
	padding: 0.5em;
}

img {
	border-radius: 5px;
	margin: auto;
}

/* Media query */

</style>