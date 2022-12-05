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

<main>
    <slot />
</main>