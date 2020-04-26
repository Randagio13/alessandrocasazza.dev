<script>
	// import Nav from "../components/Nav.svelte";
	import Stylesheet from "../components/Stylesheet.svelte";

	// export let segment;
</script>

<Stylesheet />

<!-- <Nav {segment} /> -->

<main class="relative bg-gray-100 overflow-hidden min-h-screen">
	<slot />
</main>
