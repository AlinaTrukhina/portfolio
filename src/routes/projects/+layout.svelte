<script>
	import ProjectNav from "./ProjectNav.svelte";

</script>
<div class="projects">
    <h1>My Projects</h1>
    <ProjectNav/>

    <main>
        <slot />
    </main>
</div>