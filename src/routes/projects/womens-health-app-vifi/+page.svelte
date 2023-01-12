<script>

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
    'CSS',
    'Material UI',
    'Nodemailer',
    ]

</script>

<section>
    <h1>Women's Health App - Vifi</h1>

    <h2 class=website-link><a href="hhttps://womens-health-app-vifi.herokuapp.com/">Foraging Finds website</a></h2>
    
    <a href="https://github.com/AlinaTrukhina/womens-health-app-ViFi">
        Source Code on GitHub
    </a>

</section>