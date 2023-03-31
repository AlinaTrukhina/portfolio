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