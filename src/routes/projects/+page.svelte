<!-- <script>
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
	<section>
		<h4>Explore My Recent Projects</h4>
		<br>
		<h5>You may visit the deployed version of each project at the links provided</h5>
	</section> -->
	

	<!-- <div class="imgcard">
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
	</div> -->
<!-- </section>

<style>

.projectsImgs {
	display: flex;
	flex-direction: column;
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

</style> -->

<script>

    import ffregister from '$lib/screenCaptures/ffregister.mp4';
    import ffadd from '$lib/screenCaptures/ffadd.mp4';
    import ffmap from '$lib/screenCaptures/ffmap.mp4';
    import ffedit from '$lib/screenCaptures/ffedit.mp4';
    import ffsearch from '$lib/screenCaptures/ffsearch.mp4';
    import ffimg from '$lib/images/foragingfindsimg.png';

    const source = {ffregister};
    const poster = {ffimg}

    let paused = true;

    function handleClick(e) {
        if (paused) e.target.play();
        else e.target.pause();
	}


    const techsUsed = [
    'React',
    'Redux',
    'Sagas',
    'Node.js',
    'Express',
    'PostgreSQL',
    'PassportJS',
    'Google Maps API',
    'Multer',
    'CSS',
    'Material UI'
    ]

</script>

<svelte:head>
	<title>Foraging Finds</title>
	<meta name="description" content="Foraging Finds" />
</svelte:head>

<section>
    <h1>Foraging Finds</h1>

    <h2 class=website-link>
        <a href="https://foraging-finds.herokuapp.com/" target="_blank" rel="noreferrer">
        Foraging Finds website
        </a>
    </h2>

    <h3>Duration: 2 Week Sprint</h3>

    <p>
Finding plants or mushrooms when you are out foraging is a joy! 
However, remembering the spot you found that beautiful flush of chanterelles some time after can be frustrating. 
    </p>
    <p>
This app lets foragers save their finds on a map along with a photo and a short journal entry. 
    </p>
    <p>
Users can also explore other users finds or search for a specific mushroom on a map, and leave a comment on each entry. 
    </p>
    <p>
All user entries can be viewed in a list, edited, or deleted.
    </p>

    <section class="demo">
        <h2>Demo videos</h2>
        <p>Click on video to play</p>
        <div class="demo-videos">
            <div class="screen-capture">
                <h3>Registration</h3>
                <video class="recording"
                src={ffregister}
                on:click={handleClick}
                >
                <track kind="captions">
            </div>
        
            <div class="screen-capture">
                <h3>Map</h3>
                <video class="recording"
                src={ffmap}
                on:click={handleClick}
                >
                <track kind="captions">
            </div>    
            
            <div class="screen-capture">
                <h3>Search</h3>
                <video class="recording"
                src={ffsearch}
                on:click={handleClick}
                >
                <track kind="captions">
            </div>
        
            <div class="screen-capture">
                <h3>Add Entry</h3>
                <video class="recording"
                src={ffadd}
                on:click={handleClick}
                >
                <track kind="captions">
            </div>
        
            <div class="screen-capture">
                <h3>Edit</h3>
                <video class="recording"
                src={ffedit}
                on:click={handleClick}
                >
                <track kind="captions">
            </div>
        </div>
    </section>

    <h2>Technologies Used</h2>

    <ul>
        {#each techsUsed as tech}
        <li>
            {tech}
        </li>
        {/each}
    </ul>

    <a href="https://github.com/AlinaTrukhina/solo-project-foraging-finds" target="_blank" rel="noreferrer">
        Source Code on GitHub
    </a>

</section>

<style>

.website-link a {
    color: var(--color-theme-pink);
    font-size: 0.9em;
}

.website-link a:hover {
    background-color: var(--color-theme-purple);
    padding: 5px;
    border-radius: 5px;
}

.demo-videos {
    display: flex;
    flex-wrap: wrap;
    margin-left: -1em;
    margin-top: -1em;
}

.screen-capture {
    margin: 1em;
}

</style>