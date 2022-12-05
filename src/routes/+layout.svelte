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
        (c) 2022 Alina Trukhina
    </footer>
</div>

