<script>
    import Button from './Button.svelte';

	import alinaheadshot from '$lib/images/alinaheadshot.jpg';
    import github from '$lib/images/github.svg';
    import linkedin from '$lib/images/linkedin.svg';
    import csharp from '$lib/images/csharp.svg';
    import css from '$lib/images/css.svg';
    import dotnet from '$lib/images/dotnet.svg';
    import express from '$lib/images/express.svg';
    import html5 from '$lib/images/html5.svg';
    import jquery from '$lib/images/jquery.svg';
    import js from '$lib/images/js.svg';
    import nodejs from '$lib/images/nodejs.svg';
    import pgsql from '$lib/images/pgsql.svg';
    import react from '$lib/images/react.svg';
    import redux from '$lib/images/redux.svg';
    import svelte from '$lib/images/svelte.svg';
    import materialui from '$lib/images/materialui.svg';
    import googlemapsapi from '$lib/images/googlemapsapi.svg';

</script>

<svelte:head>
    <title>Alina Trukhina Portfolio</title>
    <meta name="description" content="Alina Trukhina portfolio website" />
</svelte:head>


<section>
	<!-- <h1>About Alina</h1> -->
    <!-- <Button>
        Toggle light/dark
    </Button> -->

	<span class="heading-photo">
        <img src={alinaheadshot} alt="Alina" />
    </span>

    <div class="social-links">
        <pre>Contact: </pre>
        <a href="mailto: alina.trukhina@gmail.com"> Email</a>
        <a href="https://github.com/AlinaTrukhina">
            <img src={github} alt="GitHub">
        </a>
        <a href="https://www.linkedin.com/in/alina-trukhina/">
            <img src={linkedin} alt="LinkedIn">
        </a>
    </div>

    <article class="about-section">
        <p>
            After a decade of working in the petrochemical industry, I wanted to apply my analytical problem-solving skills in a career in tech. I have always had an interest in software development and decided to dive in head first. 
        <p>
            Software development combines my love for puzzles and always learning new technologies.
        </p>
        <p>
            My favorite hobby since the pandemic hit has been learning about native MN plants, foraging for plants, mushrooms, and going on long hikes.
        </p>
    </article>

    <article class="tech-experience">
       
            <pre>Skills </pre>
            <a href="https://html.spec.whatwg.org/multipage/">
                <img src={html5} alt="HTML">
            </a>
            <a href="https://www.w3.org/Style/CSS/#specs">
                <img src={css} alt="CSS">
            </a>
                <img src={js} alt="JS">       
                <img src={jquery} alt="jQuery">
                <img src={nodejs} alt="Node.js">
                <img src={express} alt="Express"> 
                <img src={react} alt="React"> 
                <img src={redux} alt="Redux"> 
            <a href="https://svelte.dev/">
                <img src={svelte} alt="Svelte">
            </a>
                <img src={csharp} alt="C#"> 
                <img src={dotnet} alt=".NET">
                <img src={pgsql} alt="PostgreSQL">
                <img src={materialui} alt="Material UI">
                <img src={googlemapsapi} alt="GoogleMaps API">

    </article>

</section>

<style>
:global(body) {
	min-height: 100vh;
	margin: 0;
	background-attachment: fixed;
	background-color: var(--color-theme-darkblue);
}

:global(body.light-mode) {
		background-color: #8bcbff;
		color: #22153c;
	}

pre {
    font: 1em sans-serif;
    color: var(--color-theme-pink);
}

section {
    display: flex;
    flex-direction: column;
    align-items: center;
    border: 1px;
}

article {
    width: 80vw;
    background-color: var(--color-theme-blue);
    border-radius: 10px;
    margin: 1em 0;
    padding: 1em;
}

p {
    color: var(--color-theme-pink);
}

img {
    max-width: 30em;
    border-radius: 10px;
}

.social-links{
    display: flex;
    flex-direction: row;
    align-items: center;
}
.social-links img {
    width: 2em;
    height: 2em;
    padding-left: 1em;
}

.tech-experience pre {
    font: 1.5em serif;
}

.tech-experience img {
    background-color: aliceblue;
    width: 2em;
    height: 2em;
    padding: 0.45em;
}

</style>