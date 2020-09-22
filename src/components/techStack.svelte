<!--------------------------------------------------------------------------->
<!------------------------ JAVASCRIPT DER COMPONENTE ------------------------>
<!--------------------------------------------------------------------------->
<script>
	import { fade, fly } from 'svelte/transition';
	import { onMount, onDestroy, afterUpdate} from 'svelte';
	let tog = false;

	afterUpdate(() => {
			tog = true; 
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

<div class="h-full">
{#if tog}
<div class="py-12 sm:py-16 xl:py-20 xl:px-10 xl:w-5/6 px-4 w-11/12 rounded-lg bg-gray-200 mx-auto mt-4 flex">	
	<div class="block mx-auto w-full space-y-8">
	<div class="bg-transparent text-center rounded-lg border-gray-900 border-2">
		<p class="sm:text-3xl text-xl font-bold">Technologiestack</p>
	</div>
	<div class="bg-transparent text-left">
		<p class="sm:text-xl text-lg font-bold leading-10 text-center">
		<span class="bg-red-600 text-white py-1 px-5 rounded-lg ">Svelte</span>
		<span class="bg-red-600 text-white py-1 px-5 rounded-lg ">HTML</span>
		<span class="bg-red-600 text-white py-1 px-5 rounded-lg ">TailwindCss</span>
		<span class="bg-red-600 text-white py-1 px-5 rounded-lg ">CSS</span>
		<span class="bg-red-600 text-white py-1 px-5 rounded-lg ">JavaScript</span>
		<span class="bg-red-600 text-white py-1 px-5 rounded-lg">Java</span>
		<span class="bg-red-600 text-white py-1 px-5 rounded-lg">Flutter</span>
		<span class="bg-red-600 text-white py-1 px-5 rounded-lg">Dart</span>
		<span class="bg-red-600 text-white py-1 px-5 rounded-lg">Python</span>
		</p>
	</div>
	</div>
</div>
{/if}
</div>
