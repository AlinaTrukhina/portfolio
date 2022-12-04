<script>


    // These values are bound to properties of the video
    let duration;
	let paused = true;

	// Used to track time of last mouse down event
	let lastMouseDown;

	// we can't rely on the built-in click event, because it fires
	// after a drag — we have to listen for clicks ourselves
	function handleMousedown(e) {
		lastMouseDown = new Date();
	}

	function handleMouseup(e) {
		if (new Date() - lastMouseDown < 300) {
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

    <h3>Duration: 2 Week Sprint</h3>

    <p>Finding plants or mushrooms when you are out foraging is a joy! 
        However, remembering the spot you found that beautiful flush of chanterelles some time after can be frustrating. 
        This app lets foragers save their finds on a map along with a photo and a short journal entry. </p>

    <p>Users can also explore other users finds or search for a specific mushroom on a map, and leave a comment on each entry. 
        All user entries can be viewed in a list, edited, or deleted.</p>
    
        
    
    <h2>Technologies Used</h2>

    <ul>
        {#each techsUsed as tech}
        <li>
            {tech}
        </li>
        {/each}
    </ul>
</section>