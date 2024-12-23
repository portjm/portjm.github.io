<svelte:head>
    <title>J.M. Porta</title>
</svelte:head>
<main class=" flex-grow grid p-4 bg-zinc-900 place-content-center w-screen">
    <div id="main-card" class=" h-72 w-96 p-10">
        <div id="main-card-contents">
            <h1 class="text-center">Testing Testing</h1>
            <p>
                I know absolutely nothing about CI/CD so I hope this works. 🤞
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
