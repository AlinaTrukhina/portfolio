<script>
    // scripts to import components

	import Header from './Header.svelte';
    import './styles.css'
</script>

<div class="app">
    <Header/>

    <main>
        <slot />
    </main>

    <footer>
        <p>(c) 2022 Alina Trukhina. Built with <a href="https://svelte.dev/">Svelte</a></p>
    </footer>
</div>

<style>

p {
    color: var(--color-theme-pink);
}

</style>
