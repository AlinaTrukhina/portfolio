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

.projects {
    display: flex;
}

h1 {
    text-align: center;
}

main {
    width: 80vw;
    max-height: 80vh;
    overflow-x: scroll;
    overflow-y: scroll;
    background-color: var(--color-theme-blue);
    border: 1px var(--color-theme-darkblue) solid;
    border-radius: 5px;
    padding: 1em;
}


</style>