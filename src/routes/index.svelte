<!--------------------------------------------------------------------------->
<!------------------------ JAVASCRIPT DER COMPONENTE ------------------------>
<!--------------------------------------------------------------------------->
<script>
	import WerBinIch from '../components/werBinIch.svelte';
	import Technologie from '../components/technologien.svelte';
	import TechStack from '../components/techStack.svelte';

	let cont = [
		{id: 1, name: "Ich bin nummer 1"},
		{id: 2, name: "Hallo"},
		{id: 3, name: "Hallo"},
		{id: 3, name: "Hallo"},
		{id: 3, name: "Hallo"}
	]


</script>

<!--------------------------------------------------------------------------->
<!---------------------- CSS / BOOTSTRAP DER COMPONENTE --------------------->
<!--------------------------------------------------------------------------->
<style>

</style>

<!--------------------------------------------------------------------------->
<!----------------------- HTML / MARKUP DER COMPONENTE ---------------------->
<!--------------------------------------------------------------------------->
<svelte:head>
	<title>Home</title>
</svelte:head>
<WerBinIch/>
<Technologie/>
<TechStack/>

