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
    
    <a href="https://github.com/AlinaTrukhina/weekend-jquery-server-calculator">
        Source Code on GitHub
    </a>

    <pre>
The challenge for this project was to implement a server side calculator.

The calculator interface mirrors an ordinary calculator.
The calculations are done on the server, and stored there until the user clears the inputs.
    </pre>

    <div class="screen-capture">
        <h2>Demo</h2>
        <p>Click on video to play</p>
        <video src={calculatorscreenrecording}
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

</section>

<style>

video {
    max-width: 400px;
}
</style>