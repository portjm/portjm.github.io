<svelte:head>
    <title>Portfolio [WIP]</title>
</svelte:head>
<main class=" flex-grow">
    <div class="container text-zinc-200 bg-zinc-800/85 2xl:w-2/5 mx-auto h-fit">
        <div id="main-card" class="  lg:mt-10 mt-4 mx-auto p-8 text-center">
            <h1 class="lg:text-6xl md:text-5xl text-4xl text-zinc-50 mb-0">
                J&#8855;se M. P&#8855;rta
            </h1>
            <p id="main-subhead" class="text-xl text-[#D10000] mb-6">
                Software Developer &#9663; AI Researcher
            </p>
            <p>
                I know absolutely nothing about CI/CD so I hope this works. 🤞<br
                />
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Magni iusto
                debitis, ullam dolores sapiente odit tempore maxime similique fuga
                aliquid recusandae ex harum! Ex libero dolorum assumenda officiis
                eveniet quae! Lorem ipsum dolor sit amet consectetur adipisicing
                elit. Id illum autem amet aliquam voluptatum quasi culpa, quos iste
                quod vel sit doloribus repellat illo maiores, ut provident cupiditate
                tempora! Earum. Lorem ipsum, dolor sit amet consectetur adipisicing
                elit. Asperiores laborum ex ipsum, dolores ea commodi optio sed nesciunt
                in dolorum et reiciendis odit ducimus voluptatem sint debitis fugit
                explicabo minima. Lorem ipsum dolor sit amet, consectetur adipisicing
                elit. Molestiae similique voluptatum, reprehenderit dignissimos numquam
                delectus dolore nisi alias sit aperiam atque magni ea, praesentium
                nulla ipsam ad velit accusantium! Et?
            </p>
        </div>
    </div>

    <div
        class="container text-zinc-200 bg-zinc-800/85 2xl:w-2/5 mx-auto h-fit mt-10"
    >
        <div class="p-8">
            <h1 class=" text-4xl mb-6">Technical Specs</h1>
            <div id="tech-logos">
                <img src="rs.png" width="100px" height="100px" alt="Rust" />
                <img src="py.png" width="100px" alt="Python" />
                <img src="pytor.png" width="200px" alt="PyTorch" />
                <img src="sv.png" width="100px" alt="Svelte/Sveltekit" />
            </div>
        </div>
    </div>
</main>

<style>
    #main-card {
        width: 100%;
        height: 100%;
    }

    .container {
        position: relative;
        z-index: 1;
    }

    .container::before {
        content: "";
        width: 100%;
        height: 100%;
        position: absolute;
        top: 0;
        left: 0;
        z-index: -1;
    }

    .container:hover::before {
        border: 1px solid #d10000;
    }
    #tech-logos {
        display: flex;
        justify-content: space-around;
        flex-wrap: wrap;
    }
    #tech-logos img {
        align-self: center;
    }
</style>
