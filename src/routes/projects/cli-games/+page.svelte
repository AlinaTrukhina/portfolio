<script>
	import choose_game from '$lib/images/cli_game1.png';
	import palindrome from '$lib/images/palindrome.png';
	import color_game from '$lib/images/color_game.png';
	import blackjack from '$lib/images/cli_blackjack.png';
</script>

<svelte:head>
	<title>Command Line Games</title>
	<meta name="description" content="Command Line Games" />
</svelte:head>

<section>
	<h1>Command Line interface games</h1>

	<h2 class=website-link>
        <a href="https://www.npmjs.com/package/ant-cli-game" target="_blank" rel="noreferrer">
        NPM Package
        </a>
    </h2>

	<h3>Duration: 2 Day Sprint</h3>

	<p></p>

	<div class="screen-capture">
        <h2>Screenshots</h2>
		<h4>Choose Game</h4>
		<img src={choose_game} alt="choose game" />
		<h4>Palindrom Checker</h4>
		<img src={palindrome} alt="palindrome checker" />
		<h4>Color Guessing Game</h4>
		<img src={color_game} alt="color game" />
		<h4>Blackjack</h4>
		<img src={blackjack} alt="blackjack game" />

	<h2 class="techs-used">Technologies Used</h2>
    <ul>
		<li>JavaScript</li>
	</ul>

	<a href="https://github.com/AlinaTrukhina/ant-cli-game">
        Source Code on GitHub
    </a>

</section>

<style>
	.website-link a {
		color: var(--color-theme-2);
		font-size: 0.9em;
	}

	a {
		color: var(--color-theme-pink);
		font-size: 0.9em;
	}
	
	a:hover {
		background-color: var(--color-theme-purple);
		padding: 5px;
		border-radius: 5px;
	}

	.screen-capture {
		display: flex;
		flex-direction: column;
	}

	.techs-used, .screen-capture>h2 {
		margin-bottom: 0;
	}

	img {
		max-width: 400px;
		border-radius: 5px;
	}
	
</style>