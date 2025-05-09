<script lang="ts">
	import "../app.css";

	let { children } = $props();
</script>

<div
	class="sticky top-0 z-100 shadow-md w-screen px-12 py-4 bg-indigo-800 flex flex-row justify-between text-lg text-white"
>
	<a class="font-bold" href="/">WECEAF</a>
	<div
		class="flex flex-row gap-4 [&>a]:hover:underline [&>a]:hover:cursor-pointer"
	>
		<a href="/location">Location and practicalities</a>
		<a href="/speakers">Speakers</a>
		<a href="/tickets">Tickets</a>
		<a href="/contact">Contact</a>
	</div>
</div>

<div
	class="w-screen min-h-screen bg-indigo-100 px-24 py-12 flex flex-col gap-4 items-start"
>
	{@render children()}
</div>
