<script>
	import ProjectNav from "./ProjectNav.svelte";

</script>

<h1>Projects</h1>
<div class="projects">

    <ProjectNav/>

    <main>
        <slot />
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
    position: relative;
    width: 80vw;
    max-height: 80vh;
    overflow-y: scroll;
    background-color: var(--color-theme-blue);
    border: 1px var(--color-theme-darkblue) solid;
    border-radius: 5px;
}


</style>