<script>
  import {
    Collapse,
    Navbar,
    NavbarToggler,
    NavbarBrand,
    Nav,
    NavItem,
    NavLink,
    Dropdown,
    DropdownToggle,
    DropdownMenu,
    DropdownItem
  } from 'sveltestrap';

	import { Styles } from 'sveltestrap';
	
  let isOpen = false;

  function handleUpdate(event) {
    isOpen = event.detail.isOpen;
  }
      
</script>

<Styles />

<Navbar color="dark" dark expand="md">
    <NavbarBrand href="/">Project List</NavbarBrand>
    <NavbarToggler on:click={() => (isOpen = !isOpen)} />
    <Collapse {isOpen} navbar expand="md" on:update={handleUpdate}>
      <Nav class="ms-auto" navbar>
        <NavItem>
          <NavLink href="/projects/foraging-finds">Foraging Finds</NavLink>
        </NavItem>
        <NavItem>
          <NavLink href="/projects/womens-health-directory-vifi">The ViFi, a Women's Health Directory</NavLink>
        </NavItem>
        <NavItem>
            <NavLink href="/projects/react-photo-gallery">React Photo Gallery</NavLink>
        </NavItem>        
        <NavItem>
            <NavLink href="/projects/server-side-calculator">Server-Side Calculator</NavLink>
        </NavItem>
        <NavItem>
            <NavLink href="/projects/react-redux-movie-gallery">React-Redux Movie Gallery</NavLink>
        </NavItem>
      </Nav>
    </Collapse>
</Navbar>


<style>

@import 'https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css';

nav {
    display: flex;
    flex-direction: column;
    background-color: var(--color-theme-blue);
}

nav a {
    display: block;
    min-height: 2em;
    vertical-align: center;
    border: 1px var(--color-theme-darkblue) solid;
    border-radius: 5px;
    color: var(--color-theme-pink);
    font-weight: 600;
    text-decoration: none;
    padding: 0.5em;
    overflow-wrap: break-word;
}

:global(main .light-mode) {
    background-color: var(--color-theme-blue);
}

</style>