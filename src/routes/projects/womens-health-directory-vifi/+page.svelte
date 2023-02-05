<script>

    import vifiadmincsv from '$lib/screenCaptures/vifinewslettercsv.mp4'

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
		if (new Date() - lastMouseDown < 30000) {
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
    'PassportJS',
    'CSS',
    'Material UI',
    'Nodemailer',
    ]

</script>

<svelte:head>
	<title>Women's Health Directory Web App</title>
	<meta name="description" content="Women's Health Directory Web App" />
</svelte:head>

<section>
    <h1>Women's Health App - Vifi</h1>

    <h2 class=website-link>
        <a href="https://womens-health-app-vifi.herokuapp.com/" target="_blank" rel="noreferrer">
            ViFi website
        </a>
    </h2>

    <h3>Duration: 2 Week Sprint</h3>

    <pre>
        The ViFi is a women's health directory app built for our client, Laina Latterner. 
        Laina is an enterpreneur from Minneapolis, MN.
        This app is a collaborative effort from four engineers.
    </pre>

    <pre>
        The Vifi is our client Laina Latterner's solution to the challenges of women’s health. 
        The goal of the app is to educate and support our targeted users, mainly women, 
        with access to key info about health topics in easy, concise, 
        and timely manner as well as preparation for doctor appointments so 
        women can better advocate for themselves and feel more confident about their healthcare choices. 
        As a mobile webapp, the ViFi is designed to be accessible anytime, anywhere 
        as an educative resource so women can take hold of their healthcare.
    </pre>

    <section class="demo">
        <h2>Demo videos</h2>
        <p>Click on video to play/pause</p>
        <div class="screen-capture">
            <h3>Registration</h3>
            <video src={vifiadmincsv}
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

    <a href="https://github.com/AlinaTrukhina/womens-health-app-ViFi" target="_blank" rel="noreferrer">
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

    .screen-capture > video {
        max-width: 800px;
    }
    
    </style>