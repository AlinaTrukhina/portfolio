<script>
	import ProjectNav from "./ProjectNav.svelte";

</script>
<div class="projects">
    <h1>Projects</h1>
    <ProjectNav/>

    <main>
        <slot />
    </main>
</div>

<style>

h1 {
    text-align: center;
}
</style>