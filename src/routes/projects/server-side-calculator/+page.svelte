<script>
    import calculatorscreenrecording from '$lib/screenCaptures/calculatorscreenrecording.mp4';

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
    'HTML',
    'CSS',
    'JavaScript',
    'jQuery',
    'Node.js',
    ]

</script>

<section>
    <h1>Server-Side Calculator</h1>    
    
    <h2 class=website-link>
        <a href="https://server-side-calculator-ant.herokuapp.com/" target="_blank" rel="noreferrer">
        Deployed version of the calculator
        </a>
    </h2>

    <pre>
The challenge for this project was to implement a server side calculator.

The calculator interface mirrors an ordinary calculator.
The calculations are done on the server, and stored there until the user clears the inputs.
    </pre>

    <div class="screen-capture">
        <h2>Demo</h2>
        <p>Click on video to play</p>
        <video class="recording"
        src={calculatorscreenrecording}
		on:mousedown={handleMousedown}
		on:mouseup={handleMouseup}
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
    
    <a href="https://github.com/AlinaTrukhina/weekend-jquery-server-calculator">
        Source Code on GitHub
    </a>

</section>

<svelte:head>
	<title>Server Side Calculator</title>
	<meta name="description" content="Server Side Calculator" />
</svelte:head>

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

</style>