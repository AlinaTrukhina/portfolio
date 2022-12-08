<script>
    import { page } from '$app/stores';

</script>

<section>
    <h1>Alina Trukhina</h1>
    <h2> Full Stack Software Developer</h2>

    <nav class="header-links">
        <ul>
            <li>
                <a href="/">About</a>
            </li>
            <li>|</li>
            <li>
                <a href="/projects">Projects</a>
            </li>
        </ul>
    </nav>
</section>

<style>
nav {
    display: flex;
    justify-content: center;
    --background: rgba(255, 255, 255, 0.7);
}

nav a {
    padding: 0.5rem;
    color: var(--color-text);
    font-weight: 700;
    font-size: 1.5rem;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    text-decoration: none;
    transition: color 0.2s linear;
}

a:hover {
    color: var(--color-theme-pink);
    text-decoration: underline;
}

ul {
    list-style: none;
    margin-left: 0;
    padding-left: 0;
}

li {
    display: inline;
    color: var(--color-theme-2);
}

h1 {
    font-size: 2em;
    letter-spacing: 0.1em;
    text-align: center;
}

h2 {
    text-align: center;
}

</style>