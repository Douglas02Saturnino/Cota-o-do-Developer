<script>
    import Card from "./Card.svelte"

    let jobs = [
        {
            id: 1,
            name: "Youtube Video",
            "daily-hours": 1,
            "total-hours": 4,
            created_at: new Date(),
            status: 'Em progresso',
            budget: 100
        },
        {
            id: 2,
            name: "Podcast",
            "daily-hours": 1,
            "total-hours": 3,
            created_at: new Date(),
            status: 'Encerrado',
            budget: 200
        }
    ]
</script>

<div class="max-w-4xl mx-auto -mt-8">
    <main class="animate-up delay-2">
        <h1 class="sr-only">Trabalhos</h1>
        <div class="cards space-y-2">
            {#each jobs as job (job.id)}
            <Card {job} />
            {/each}
    </div>
    </main>
</div>