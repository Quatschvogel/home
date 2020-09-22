<!--------------------------------------------------------------------------->
<!------------------------ JAVASCRIPT DER COMPONENTE ------------------------>
<!--------------------------------------------------------------------------->
<script>
	import { fade, fly } from 'svelte/transition';
	import { onMount, onDestroy, afterUpdate } from 'svelte';
	let tog = false;

	afterUpdate(() => {
		setTimeout(toggle, 500)
		function toggle() {
			tog = true; 
		}
	});

	onDestroy(() => {
		tog = false;
	});
</script>

<!--------------------------------------------------------------------------->
<!---------------------- CSS / BOOTSTRAP DER COMPONENTE --------------------->
<!--------------------------------------------------------------------------->
<style>

</style>

<!--------------------------------------------------------------------------->
<!----------------------- HTML / MARKUP DER COMPONENTE ---------------------->
<!--------------------------------------------------------------------------->
{#if tog}
<div class="py-12 sm:py-16 xl:py-20 xl:px-10 xl:w-5/6 px-4 w-11/12 rounded-lg bg-gray-200 mx-auto mt-8 flex" in:fade="{{x:0, duration: 1000}}">	
	<div class="block mx-auto w-full space-y-8">
	<div class="bg-transparent text-center rounded-lg border-gray-900 border-2" in:fly="{{x: -2000, duration: 1000}}">
		<p class="sm:text-3xl text-xl font-bold">Wer Bin ich?</p>
	</div>
	<div class="bg-transparent text-left rounded-lg border-gray-900 border-2" in:fly="{{y: -50, delay: 1100, duration: 1000}}">
		<p class="sm:text-xl text-lg font-bold p-4">
			Ich bin ein Frontend und Backend Softwareentwickler für Websiten und APP´s. Für ihren Erfolg setzte ich
			auf moderne technologien um mit dem Puls der Zeit zu gehen. Dieser Einsatz ist auch für ihr Business
			von Vorteil, da die Webseiten beispielsweise 100% SEO und 100% der möglichen Performance besitzen.
		</p>
	</div>
	</div>
</div>
{/if}