<script lang="ts">
	import "../app.css";

	import elenut from "$lib/assets/elenut.svg";
	import nutrilogix from "$lib/assets/nutrilogix.svg";

	let { children } = $props();
</script>

<div class="flex flex-col min-h-screen">
	<div
		class="sticky top-0 z-100 w-screen px-12 py-4 bg-indigo-800 flex flex-row justify-between text-lg text-white"
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
		class="w-screen grow bg-indigo-100 px-24 py-12 flex flex-col gap-4 items-start"
	>
		{@render children()}
	</div>
	
	<div class="w-screen px-24 py-12 bg-indigo-800 grid grid-cols-3 gap-6 text-white text-sm">
		<div>
			<p>Western European Conference on Elephant Auto-Fellatio is a registered trademark of Giulio Il Nero Events. All rights reserved.</p>
			<hr class="stroke-white my-4">
			<p>Rue Clarence Préviot 73</p>
			<p>1002 Brussels</p>
			<p>Belgium</p>
			<hr class="stroke-white my-4">
			<p>VAT: BTW BE0437 276 121</p>
		</div>
		<div class="flex flex-col gap-2">
			<a href="mailto:info@weceaf.be" class="underline">Contact us</a>
			<a href="mailto:joris.wouters@weceaf.be" class="underline">Press</a>
			<a href="mailto:pieter.provoost@weceaf.be" class="underline">Is oatmeal really that healthy?</a>

		</div>
		<div>
			<p>The WECEAF is made possible thanks to the generous sponsoring of:</p>
			<div class="flex flex-row gap-4 mt-8 w-full [&>img]:flex-1">
				<img class="w-full" src={elenut} alt="Elenut logo">
				<img class="w-full" src={nutrilogix} alt="Nutrilogix logo">
			</div>
		</div>
	</div>
</div>