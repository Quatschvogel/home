<!--------------------------------------------------------------------------->
<!------------------------ JAVASCRIPT DER COMPONENTE ------------------------>
<!--------------------------------------------------------------------------->
<script>
	export let segment;
	
	// Scrolling position
	let y = 0;


</script>

<!--------------------------------------------------------------------------->
<!---------------------- CSS / BOOTSTRAP DER COMPONENTE --------------------->
<!--------------------------------------------------------------------------->
<style>
	.transText {
		transition: margin 200ms ease-in-out;
	}
	.transBackground {
		transition: background-color 100ms;
		transition: border-radius 500ms;
	}
	.transPadding {
		transition: margin 200ms ease-in-out;
	}
</style>

<!--------------------------------------------------------------------------->
<!----------------------- HTML / MARKUP DER COMPONENTE ---------------------->
<!--------------------------------------------------------------------------->
<svelte:window bind:scrollY={y}/>

<header class="{y < 8 ? 'bg-transparent' : 'bg-gray-800 rounded-b-lg '}  items-center flex justify-between py-4 sticky top-0 z-10 transBackground sm:py-6">
	<div class="{y < 8 ? 'text-black bg-red-500 hover:bg-red-700 ml-10' : 'text-white hover:bg-gray-800 ml-4'} text-lg sm:text-2xl font-semibold transPadding rounded-full px-4">
		Logo
	</div>
	<div class="{y < 8 ? 'space-x-5 sm:space-x-20 mr-4' : 'space-x-2 sm:space-x-10 mr-0'} transText text-lg px-4 sm:text-2xl">
		<a class="{y < 8 ? 'text-black bg-red-500 hover:bg-red-700' : 'text-white hover:bg-gray-800'} rounded px-2 py-1 transText" aria-current="{segment === undefined ? 'page' : undefined}" href=".">Home</a>
		<a class="{y < 8 ? 'text-black bg-red-500 hover:bg-red-700': 'text-white hover:bg-gray-800'} rounded px-2 py-1 transText" aria-current="{segment === 'about' ? 'page' : undefined}" href="about">Kontakt</a>
	</div>
</header>