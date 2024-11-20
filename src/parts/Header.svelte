<script>
    import { app } from '../store.js';
    export let title;

    function goToHome(){
        $app.page = 'home'
    }
</script>

<header class="py-10 bg-gray-700 px-4">
    <div class="animete-up text-gray-400 font-semibold flex itemns-center">
        <button on:click={goToHome}>
            <img src="/images/back.svg" alt="">
        </button>
        <h1 class="mx-auto">{ title }</h1>
    </div>
</header>