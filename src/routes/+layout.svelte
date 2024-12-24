<script>
    import "../app.css";

    let { children } = $props();
</script>

<div class="flex flex-col min-h-screen bg-zinc-900">
    <header
        class=" h-20 bg-zinc-950 content-center border-solid border-b-2 border-[#D10000] font-serif"
    >
        <h1 class=" text-5xl text-slate-200 sm:pl-9 sm:text-left text-center">
            Portfolio
        </h1>
    </header>
    {@render children()}
</div>
