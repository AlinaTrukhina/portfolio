<script>
	import ProjectNav from "./ProjectNav.svelte";

</script>

<h1>Projects</h1>
<div class="projects">

    <ProjectNav/>

    <main>
        <slot>
            <a class="block" href="/projects/foraging-finds">
                Foraging Finds
            </a>
        </slot>
    </main>
</div>

<style>

@import 'https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css';

.projects {
    display: flex;
    flex-direction: column;
}

h1 {
    text-align: center;
}

main {
    max-width: 100vw;
    max-height: 100vh;
    overflow-x: scroll;
    overflow-y: scroll;
    scrollbar-color: var(--color-theme-blue);
    background-color: var(--color-theme-blue);
    border: 1px var(--color-theme-darkblue) solid;
    border-radius: 5px;
    padding: 1em;
}

@media only screen and (min-width: 768px) {
    main {
        margin-right: 1em;
        width: 80vw;
    }
}
</style>