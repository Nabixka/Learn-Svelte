<script>
	let { children } = $props();
	import "../app.css"

	
</script>

<nav class="flex w-full py-2 bg-gray-800 text-white gap-5 pl-5	">
	<a href="/">Dashboard</a>
	<a href="/state">State</a>
</nav>

{@render children()}
