<script>
    let freeHours = 1;
    let profile = {
        name: "Douglas Saturnino",
        avatar: "htpps://github.com/maykbrito.png"
    };

    let statusCount= {
        total: 2,
        done: 1,
        progress: 1
    }
</script>

<header class="page-header bg-gray-700 text-white p-4 pb-8">
    <div class="max-w-4xl">
        <section id="top" 
                 class="animete-up flex 
                        justify-between 
                        items-center border-b 
                        border-b-gray-600 pg-8">
            <h2 class="sr-only">Homepage</h2>
            <img id="logo" src="/images/logo.svg" alt="logo"/>
            <span id="notification" class="flex gap-2">
                <img class="w-6" src="/images/alert-octagon.svg" alt="Alerta"/>
                {#if freeHours <=0}
                    Você não tem horas livres
                {:else}
                    Você tem {freeHours} {freeHours ==1 ? 'hora livre' : 'horas livres'} horas livres no seu dia
                    {/if}
            </span>
            <button id="avatar-profile" class='flex items-center gap-4 hover:text-orange-400 transition'>
                <div class="grid text-end">
                    <strong>{profile.name}</strong>
                    <span class="text-xs+">Ver perfil</span>
                </div>
                <img class="w-16 border-2 border-orange-400 rounded-full" src={profile.avatar} alt="Avatar do perfil"/>
            </button>
        </section>
        <div class="separator"></div>

        <section id="sumary" class="animate-up delay-1 flex justify-between items-center">
            <h2 class="sr-only">Sumário</h2>
            <div class="info flex gap-8 py-8">
                <div class="total grid">
                    <strong class="text-xl">{statusCount.total}</strong>
                    Projetos ao total
                </div>
                <div class="in-progress">
                    <strong class="text-xl">{statusCount.progress}</strong>
                    Em andamento
                </div>
                <div class="finished">
                    <strong class="text-xl">{statusCount.done}</strong>
                    Encerrados
                </div>
            </div>
            <button class="button orange uppercase flex gap-4 
                         bg-orange-400 h-fit px-3 py-2 rounded
                           items-center hover:brightness-110 transition-all">
                <span class="bg-opacity-10 bg-white rounded p-0.5">
                    <img src="/images/plus-24.svg" alt="Novo Job">
                </span>
                <p class="px-2 text-xs font-bold">
                    Novo projeto
                </p>
            </button>
        </section>
    </div>
</header>