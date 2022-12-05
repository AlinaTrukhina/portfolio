<script>
	import alinaheadshot from '$lib/images/alinaheadshot.jpg';
    import github from '$lib/images/github.svg';
    import linkedin from '$lib/images/linkedin.svg';
</script>

<svelte:head>
    <title>Alina Trukhina Portfolio</title>
    <meta name="description" content="Alina Trukhina portfolio website" />
</svelte:head>


<section>
	<!-- <h1>About Alina</h1> -->

	<span class="heading-photo">
        <img src={alinaheadshot} alt="Alina" />
    </span>

    <div class="social-links">
        <p>Contact: </p>
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

</section>

<style>

section {
    display: flex;
    flex-direction: column;
    align-items: center;
    border: 1px;
}


.about-section {
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

</style>