<script>
	let { children } = $props();
	import "../app.css"
</script>

<nav class="bg-gray-900 text-white py-2 flex justify-between pl-10 pr-10">
	<a href="/dashboard">Dashboard</a>
	<span class="flex gap-10">
		<a href="/auth/login">Login</a>
		<a href="/auth/register">Register</a>
	</span>
</nav>

{@render children()}

<footer>
	<h3>All Right</h3>
</footer>