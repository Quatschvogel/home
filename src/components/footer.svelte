<!--------------------------------------------------------------------------->
<!------------------------ JAVASCRIPT DER COMPONENTE ------------------------>
<!--------------------------------------------------------------------------->
<script>
    import { onMount, onDestroy, afterUpdate } from 'svelte';
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
{#if tog}
<footer class="w-full h-auto bg-gray-800 mt-4 rounded-t-lg align-bottom relative bottom-0">
    <div class="block w-full">
        <div class="flex justify-between">
            <img class="py-2 h-20 pl-5" alt="logo" src="logo-192.png"/>
            <p class="text-white my-auto pr-5 font-semibold">Hier sind Die Icons</p>
        </div>
    </div>
</footer>
{/if}