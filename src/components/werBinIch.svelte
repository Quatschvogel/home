<!--------------------------------------------------------------------------->
<!------------------------ JAVASCRIPT DER COMPONENTE ------------------------>
<!--------------------------------------------------------------------------->
<script>
	import { fade, fly } from 'svelte/transition';
	import {onMount, beforeUpdate, afterUpdate, onDestroy} from 'svelte';
	let tog = false;
	let y;
	let a = 0;
	afterUpdate(() => {
		if (process.browser) {
			a = 1;
		}
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
<svelte:window bind:scrollY={y}/>
<div class="py-12 sm:py-16 xl:py-20 xl:px-10 xl:w-5/6 px-4 w-11/12 rounded-lg bg-gray-200 mx-auto mt-8 flex">	
	<div class="block mx-auto w-full space-y-8">
	<div on:click={() => {tog = !tog}} class="bg-transparent text-center rounded-lg border-gray-900 border-2 cursor-pointer hover:bg-gray-400" >
		<p class="sm:text-3xl text-xl font-bold">Wer Bin ich?</p>
	</div>
	{#if a >= 1}
	<div class="bg-transparent text-left rounded-lg border-gray-900 border-2" in:fly="{{y: -100, duration: 1000}}">
		<p class="sm:text-xl text-lg font-bold p-4">
			Ich bin ein Frontend und Backend Softwareentwickler für Websiten und APP´s. Für ihren Erfolg setzte ich
			auf moderne technologien um mit dem Puls der Zeit zu gehen. Dieser Einsatz ist auch für ihr Business
			von Vorteil, da die Webseiten beispielsweise 100% SEO und 100% der möglichen Performance besitzen.
		</p>
	</div>
	{/if}
	</div>
</div>