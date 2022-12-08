<script>
    import ffregister from '$lib/screenCaptures/ffregister.mp4';
    import ffadd from '$lib/screenCaptures/ffadd.mp4';
    import ffmap from '$lib/screenCaptures/ffmap.mp4';
    import ffedit from '$lib/screenCaptures/ffedit.mp4';
    import ffsearch from '$lib/screenCaptures/ffsearch.mp4';

    // These values are bound to properties of the video
	let paused = true;

	// Used to track time of last mouse down event
	let lastMouseDown;

	// we can't rely on the built-in click event, because it fires
	// after a drag — we have to listen for clicks ourselves
	function handleMousedown(e) {
		lastMouseDown = new Date();
	}

	function handleMouseup(e) {
		if (new Date() - lastMouseDown < 3000) {
			if (paused) e.target.play();
			else e.target.pause();
		}
	}

    const techsUsed = [
    'React',
    'Redux',
    'Sagas',
    'Node.js',
    'Express',
    'PostgreSQL',
    'Passport',
    'Google Maps API',
    'Multer',
    'CSS',
    'Material UI'
    ]

</script>

<section>
    <h1>Foraging Finds</h1>

    <a href="https://github.com/AlinaTrukhina/solo-project-foraging-finds">
        Source Code on GitHub
    </a>

    <h3>Duration: 2 Week Sprint</h3>

    <pre>
Finding plants or mushrooms when you are out foraging is a joy! 
However, remembering the spot you found that beautiful flush of chanterelles some time after can be frustrating. 
  
This app lets foragers save their finds on a map along with a photo and a short journal entry. 

Users can also explore other users finds or search for a specific mushroom on a map, and leave a comment on each entry. 
  
All user entries can be viewed in a list, edited, or deleted.
    </pre>
    
    <section class="demo">
        <h2>Demo videos</h2>
        <p>Click on video to play</p>
        <div class="screen-capture">
            <h3>Registration</h3>
            <video src={ffregister}
            on:mousedown={handleMousedown}
            on:mouseup={handleMouseup}
            bind:paused>
            <track kind="captions">
        </div>
    
        <div class="screen-capture">
            <h3>Map</h3>
            <video src={ffmap}
            on:mousedown={handleMousedown}
            on:mouseup={handleMouseup}
            bind:paused>
            <track kind="captions">
        </div>    
        
        <div class="screen-capture">
            <h3>Search</h3>
            <video src={ffsearch}
            on:mousedown={handleMousedown}
            on:mouseup={handleMouseup}
            bind:paused>
            <track kind="captions">
        </div>
    
        <div class="screen-capture">
            <h3>Add Entry</h3>
            <video src={ffadd}
            on:mousedown={handleMousedown}
            on:mouseup={handleMouseup}
            bind:paused>
            <track kind="captions">
        </div>
    
        <div class="screen-capture">
            <h3>Edit</h3>
            <video src={ffedit}
            on:mousedown={handleMousedown}
            on:mouseup={handleMouseup}
            bind:paused>
            <track kind="captions">
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
</section>