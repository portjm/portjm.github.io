<script>
    let { name = "Project 0", description } = $props();
</script>

<div class=" bg-slate-300 p-4 pb-6">
    <h3 class=" text-2xl text-zinc-800 font-semibold">{name}</h3>
    <p class="text-zinc-500 text-sm">subheader</p>
    {#if description}
        <p class="mt-4 text-zinc-800">
            {@render description()}
        </p>
    {/if}
</div>
