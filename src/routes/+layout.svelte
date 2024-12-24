<script>
    import "../app.css";

    let { children } = $props();
</script>

<div class=" grid-background flex flex-col min-h-screen bg-zinc-900">
    <header
        class=" h-20 bg-zinc-950 content-center border-solid border-b-2 border-[#D10000] font-serif"
    >
        <h1 class=" text-5xl text-slate-200 sm:pl-9 sm:text-left text-center">
            J.M. P&#9676;rta
        </h1>
    </header>
    {@render children()}
</div>

<style>
    .grid-background {
        background-size: 40px 40px;
        position: relative;
        background-image: linear-gradient(
                to right,
                rgb(75, 75, 75) 1px,
                transparent 1px
            ),
            linear-gradient(to bottom, rgb(75, 75, 75) 1px, transparent 1px);
    }
</style>
