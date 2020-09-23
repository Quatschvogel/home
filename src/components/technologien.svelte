<!--------------------------------------------------------------------------->
<!------------------------ JAVASCRIPT DER COMPONENTE ------------------------>
<!--------------------------------------------------------------------------->
<script>
	import { fade, fly } from 'svelte/transition';
	import {onMount, beforeUpdate, afterUpdate, onDestroy} from 'svelte';
	let tog = false;
	afterUpdate(() => {
		if (process.browser && window) {
			tog = true;
		}
	});
</script>

<!--------------------------------------------------------------------------->
<!---------------------- CSS / BOOTSTRAP DER COMPONENTE --------------------->
<!--------------------------------------------------------------------------->
<style>

	.transitionRL {
		animation: flyinRL 1s ease forwards;
	}

	.transitionLR {
		animation: flyinLR 1s ease forwards;
	}

	@keyframes flyinRL {
		0% {
			transform: translateX(200%);
			opacity: 0;
		}
		100% {
			transform: translateX(0%);
			opacity: 1;
		}
	}

	@keyframes flyinLR {
		0% {
			transform: translateY(-50%);
			opacity: 0;
		}
		100% {
			transform: translateY(0%);
			opacity: 1;
		}
	}
</style>

<!--------------------------------------------------------------------------->
<!----------------------- HTML / MARKUP DER COMPONENTE ---------------------->
<!--------------------------------------------------------------------------->
{#if tog == true}
<div class="py-12 sm:py-16 xl:py-20 xl:px-10 xl:w-5/6 px-4 w-11/12 rounded-lg bg-gray-200 mx-auto mt-4 flex">	
	<div class="block mx-auto w-full space-y-8">
	<div class="bg-transparent text-center rounded-lg border-gray-900 border-2 transitionLR">
		<p class="sm:text-3xl text-xl font-bold">Welche Technologien kommen zum Einsatz?</p>
	</div>

	<div class="bg-transparent text-left rounded-lg border-gray-900 border-2 transitionRL" >
		<p class="sm:text-xl text-lg font-bold p-4">
			Ich bin ein Frontend und Backend Softwareentwickler für Websiten und APP´s. Für ihren Erfolg setzte ich
			auf moderne technologien um mit dem Puls der Zeit zu gehen. Dieser Einsatz ist auch für ihr Business
			von Vorteil, da die Webseiten beispielsweise 100% SEO und 100% der möglichen Performance besitzen.
		</p>
	</div>

	</div>
</div>
{/if}
