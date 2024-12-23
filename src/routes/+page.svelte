<svelte:head>
    <title>J.M. Porta</title>
</svelte:head>
<main class=" flex-grow grid p-4 bg-zinc-900 place-content-center w-screen">
    <div id="main-card" class=" h-72 w-96 p-10">
        <div id="main-card-contents">
            <h1 class="text-center">Welcome to SvelteKit</h1>
            <p>
                Visit <a href="https://svelte.dev/docs/kit"
                    >svelte.dev/docs/kit</a
                > to read the documentation
            </p>
        </div>
    </div>
</main>

<style>
    h1 {
        @apply text-3xl;
    }
    #main-card {
        position: relative;
        z-index: 2;
        background-color: whitesmoke;
    }

    #main-card-contents {
        position: relative;
        z-index: 1;
    }
</style>
