<script>
	import Nav from '../components/Nav.svelte';
	import Footer from '../components/footer.svelte';

	export let segment;
</script>

<style>

</style>
<div class="flex flex-col min-h-screen">
<Nav {segment}/>
	<slot></slot>
<div class="flex-grow"></div>
<Footer/>
</div>