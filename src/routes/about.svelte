<!--------------------------------------------------------------------------->
<!------------------------ JAVASCRIPT DER COMPONENTE ------------------------>
<!--------------------------------------------------------------------------->
<script>
    import {fade} from 'svelte/transition'

    let valueTextArea;
    let valueInput;

    function clear() {
        valueTextArea = '';
        valueInput = '';
    }
</script>

<!--------------------------------------------------------------------------->
<!---------------------- CSS / BOOTSTRAP DER COMPONENTE --------------------->
<!--------------------------------------------------------------------------->
<style>
    .borderNeu {
        border-width: 1px;
    }
</style>

<!--------------------------------------------------------------------------->
<!----------------------- HTML / MARKUP DER COMPONENTE ---------------------->
<!--------------------------------------------------------------------------->
<svelte:head>
    <title>Kontakt</title>
</svelte:head>

<div class="py-12 sm:py-16 xl:py-20 xl:px-10 xl:w-5/6 px-4 w-11/12 rounded-lg bg-gray-200 mx-auto mt-8 flex font-semibold" in:fade="{{x:0, duration: 1000}}">	
    <p>
        Falls sie Fragen haben sollten oder ein Individuelles angebot für die Erstellung ihrer Eigenen Webseite
        haben wollen, füllen sie dieses Formular aus und ich werde mich bei Ihnen melden.
    </p>
</div>
<div class="pt-6 sm:pt-8 xl:pt-8 xl:px-10 xl:w-5/6 pb-4 px-4 w-11/12 rounded-lg bg-gray-200 mx-auto mt-8 flex font-semibold" in:fade="{{x:0, duration: 1000}}">	
    <div class="w-full">
        <p>Email Adresse:</p>
        <input bind:value={valueInput} type="text" class="w-full borderNeu border-gray-800 rounded-md p-2">
        <p class="pt-4">Anliegen:</p>
        <textarea bind:value={valueTextArea} name="" id="" cols="30" rows="10" class="resize-none w-full borderNeu border-gray-800 rounded-md p-2"></textarea>
    <div class="flex pt-4 space-x-5">    
        <button class="bg-green-700 p-2 rounded-md text-white font-semibold hover:bg-green-500">Senden</button>
        <button on:click={clear} class="bg-green-700 p-2 rounded-md text-white font-semibold hover:bg-green-500">Abbrechen</button>
    </div>
    </div>
</div>
