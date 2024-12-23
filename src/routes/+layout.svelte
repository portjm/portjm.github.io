<script>
    import "../app.css";

    let { children } = $props();
</script>

<div class="flex flex-col min-h-screen">
    <header
        class=" h-20 bg-zinc-900 content-center border-solid border-b-2 border-slate-300 font-serif"
    >
        <h1 class=" text-5xl text-slate-50 pl-9">Portfolio</h1>
    </header>
    {@render children()}
</div>
