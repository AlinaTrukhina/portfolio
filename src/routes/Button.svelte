<script>
let darkMode = true;
function toggle() {
	darkMode = !darkMode;
	window.document.body.classList.toggle('light-mode');
	window.document.main.classList.toggle('light-mode');
	window.document.article.classList.toggle('light-mode');
	window.document.h1.classList.toggle('light-mode');
	window.document.h2.classList.toggle('light-mode');
	window.document.h3.classList.toggle('light-mode');
	window.document.h4.classList.toggle('light-mode');
	window.document.h5.classList.toggle('light-mode');
	window.document.h6.classList.toggle('light-mode');
	window.document.p.classList.toggle('light-mode');
}
</script>
<button on:click={toggle}>
	{#if darkMode }
		Go light
	{:else}
		Go dark
	{/if}
</button>

<style>
	button {
		background-color: var(--color-theme-pink);
		color: var(--color-theme-darkblue);
		border: none;
		border-radius: 4px;
		padding: 0.5rem;
		text-transform: uppercase;
	}
	:global(body.light-mode) button {
		background-color: #0084f6;
		color: white;
	}
</style>