<script>
    import PCard from "$lib/components/PCard.svelte";
</script>

<svelte:head>
    <title>Portfolio [WIP]</title>
</svelte:head>
<main class=" flex-grow">
    <div class="container text-zinc-200 bg-zinc-800/85 2xl:w-2/5 mx-auto h-fit">
        <div id="main-card" class="  lg:mt-10 mt-4 mx-auto p-8 text-center">
            <h1 class="lg:text-6xl md:text-5xl text-4xl text-zinc-50 mb-0">
                Jose M. Porta
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
        class="container text-zinc-200 bg-zinc-800/85 2xl:w-2/5 mx-auto h-fit mt-8"
    >
        <div class="md:p-6 p-3">
            <h1 class=" text-4xl mb-6">Technical Specs</h1>
            <div id="tech-logos" class="md:mx-0 mx-3">
                <img src="rs.png" width="100px" height="100px" alt="Rust" />
                <img src="py.png" width="100px" alt="Python" />
                <img src="pytor.png" width="200px" alt="PyTorch" />
                <img src="sv.png" width="100px" alt="Svelte/Sveltekit" />
                <img src="cuda.png" width="200px" alt="PyTorch" />
            </div>
        </div>
    </div>

    <div
        class="container text-zinc-200 bg-zinc-800/85 2xl:w-2/5 mx-auto h-fit mt-8"
    >
        <div class="md:p-6 p-3">
            <h1 class=" text-4xl mb-6">Projects</h1>
            <div class="grid lg:grid-cols-2 gap-4 gap-y-8 items-start w-full">
                <PCard name="Project 0">
                    {#snippet description()}
                        <img
                            src="https://placehold.co/600x300"
                            alt="placeholder"
                        /><br />
                        Lorem ipsum dolor sit amet consectetur adipisicing elit.
                        Minus labore a reprehenderit. Enim earum nam, quam tenetur
                        itaque doloribus reprehenderit voluptate hic expedita at
                        fugit dolores adipisci blanditiis, mollitia qui!
                    {/snippet}
                </PCard>
                <PCard name="Project 1">
                    {#snippet description()}
                        <img
                            src="https://placehold.co/600x300"
                            alt="placeholder"
                        /><br />
                        Lorem ipsum dolor sit amet consectetur adipisicing elit.
                        Exercitationem dicta officia aliquam sit magni dignissimos
                        labore placeat numquam id iste fugiat molestiae natus architecto
                        dolore, impedit, iusto saepe tempora ipsum!
                    {/snippet}
                </PCard>
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
        box-shadow: 0px 0px 10px #d1000077;
    }
    #tech-logos {
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
    }
    #tech-logos img {
        align-self: center;
    }
</style>
