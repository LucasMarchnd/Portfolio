<script>
    export let title;
    export let icons; 
</script>

<div class="flex justify-between items-center py-4">
    <div class="text-left">
        <h3 class="text-xl font-bold">{title}</h3>
    </div>

    <div class="lg:flex lg:space-x-4 grid grid-cols-2 gap-4 md:grid-cols-4">
        {#each icons as icon}
            <div class="flex flex-col items-center">
                <img src={icon.src} alt={icon.alt} class="w-10 h-10" style="filter: invert(1);">
                <p class="text-white mt-2">{icon.alt}</p>
            </div>
        {/each}
    </div>
</div>