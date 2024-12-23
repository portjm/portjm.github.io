<script>
    import { onMount } from "svelte";
    let alpha = 0.333;
    let beta = 0.2;
    function draw_canvas(context) {
        context.beginPath();
        context.arc(500, 500, 500, 0, Math.PI, true);
        context.strokeStyle = "red";
        context.lineWidth = 10;
        context.fillStyle = "wheat";
        context.stroke();
        context.fill();
    }

    function draw_grid(context, a, b) {
        for (let i = 0; i < 63; i++) {
            for (let j = 0; j < 29; j++) {
                context.beginPath();
                context.arc(i * 20 + 5, j * 20 + 5, j, 0, 2 * Math.PI);
                // context.strokeStyle = "red";
                // context.lineWidth = 1;
                context.fillStyle = "black";
                context.stroke();
                context.fill();
            }
        }

        context.fillStyle = "rgb(255 255 255 / 25%)";
        context.fillRect(0, 0, 2000, 1000);
    }

    function apply_bg(canvas) {
        var data_url = canvas.toDataURL();
        document.getElementById("main-card").style.background =
            `url(${data_url})`;
    }
    onMount(() => {
        const cnv = document.getElementById("bg-canvas");
        const ctx = cnv.getContext("2d");
        draw_grid(ctx, alpha, beta);
        apply_bg(cnv);
        // const interval = setInterval(() => {
        //     draw_grid(ctx, alpha, beta);
        //     apply_bg(cnv);
        //     alpha = alpha + 0.01;
        //     beta = beta + 0.01;
        // }, 1000);
    });
</script>

<svelte:head>
    <title>J.M. Porta</title>
</svelte:head>
<main
    class=" flex-grow grid grid-rows-2 gap-4 p-4 bg-zinc-900 place-content-center w-screen"
>
    <div
        id="main-card"
        class=" flex-grow content-center px-16 py-10 rounded-lg"
    >
        <div id="main-card-contents" class="text-center">
            <h1 class="text-5xl text-zinc-50 mb-4">Testing Testing</h1>
            <p>
                I know absolutely nothing about CI/CD so I hope this works. 🤞
            </p>
            <br />
            <p>
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Magni
                iusto debitis, ullam dolores sapiente odit tempore maxime
                similique fuga aliquid recusandae ex harum! Ex libero dolorum
                assumenda officiis eveniet quae! Lorem ipsum dolor sit amet
                consectetur adipisicing elit. Id illum autem amet aliquam
                voluptatum quasi culpa, quos iste quod vel sit doloribus
                repellat illo maiores, ut provident cupiditate tempora! Earum.
                Lorem ipsum, dolor sit amet consectetur adipisicing elit.
                Asperiores laborum ex ipsum, dolores ea commodi optio sed
                nesciunt in dolorum et reiciendis odit ducimus voluptatem sint
                debitis fugit explicabo minima. Lorem ipsum dolor sit amet,
                consectetur adipisicing elit. Molestiae similique voluptatum,
                reprehenderit dignissimos numquam delectus dolore nisi alias sit
                aperiam atque magni ea, praesentium nulla ipsam ad velit
                accusantium! Et?
            </p>
        </div>
    </div>
    <div class=" bg-stone-500 px-16 py-10">
        <h2 class=" text-3xl text-zinc-300 text-center mb-3">PROJECTS</h2>
    </div>
</main>
<canvas width="2000" height="1000" id="bg-canvas"></canvas>

<style>
    #main-card {
        position: relative;
        z-index: 2;
        /* background-color: rgba(240, 240, 240, 0.4); */
    }
    #main-card-contents p {
        color: rgb(184, 184, 184);
    }
    canvas {
        display: none;
    }
</style>
