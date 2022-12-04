<script>
    import galleryrecording from '$lib/screenCaptures/galleryscreenrecording.mp4';

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
    'Node.js',
    'PostgreSQL',
    'HTML',
    'CSS',
    'Material UI'
]
</script>

<section class="projectReactGallery">
    <h1>React Photo Gallery</h1>    
    
    <a href="https://github.com/AlinaTrukhina/weekend-react-gallery">
        Source Code on GitHub
    </a>

    <p>This app shows photos in a beautiful gallery format, 
        where you can click on an image to display it description. 
        Clicking the description displays the image.
    </p>
    <p>
        You can also like any image by clicking the heart icon, 
        or delete it with the trash can icon.
    </p>
    <p>
        You can add your own photo to the gallery by entering 
        the url and description and clicking submit photo.
    </p>
        
    <div class="screen-capture">
        <h2>Demo</h2>
        <p>Click on video to play</p>
        <video src={galleryrecording}
		on:mousedown={handleMousedown}
		on:mouseup={handleMouseup}
		bind:duration
		bind:paused>
        <track kind="captions">
    </div>
    <h2>Technologies Used</h2>
    <ul>
        {#each techsUsed as tech}
        <li>
            {tech}
        </li>
        {/each}
    </ul>

</section>

<style>

video {
    max-width: 600px;
}
</style>