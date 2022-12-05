<script>
    // scripts to import components
    import github from '$lib/images/github.svg';
    import linkedin from '$lib/images/linkedin.svg';
	import Header from './Header.svelte';
    import './styles.css'
</script>

<div class="app">
    <Header/>

    <main>
        <slot />
    </main>

    <footer>
        (c) 2022 Alina Trukhina
        <div class="social-links">
            <a href="https://github.com/AlinaTrukhina">
                <img src={github} alt="GitHub">
            </a>
            <a href="https://www.linkedin.com/in/alina-trukhina/">
                <img src={linkedin} alt="LinkedIn">
            </a>
        </div>
    </footer>
</div>

<style>
    /* social  */
    .social-links img {
        width: 2em;
        height: 2em;
    }
</style>