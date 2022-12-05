<!-- // scripts -->
<script>
	import Gallery from "./react-photo-gallery/+page.svelte";
      
</script>

<aside class="sidebar">
  <nav>    
    <a class="block" href="/projects/foraging-finds">
        Foraging Finds
    </a>
    <a class="block" href="/projects/react-photo-gallery">
        React Photo Gallery
    </a>
    <a class="block" href="/projects/react-redux-movie-gallery">
        React-Redux Movie Gallery
    </a>
    <a class="block"  href="/projects/server-side-calculator">
        Server-Side Calculator
    </a>
  </nav>
</aside>

<style>
.sidebar {
    width: 20%;
}
nav {
    display: flex;
    flex-direction: column;
    background-color: var(--color-theme-blue);
}

nav a {
    display: block;
    height: 2em;
    border: 1px var(--color-theme-darkblue) solid;
    color: var(--color-theme-pink);
    font-weight: 500;
    text-decoration: none;
    padding: 0.5em;
}
</style>