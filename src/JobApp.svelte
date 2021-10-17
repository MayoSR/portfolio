<div class="main-app">
    <div class="app-desc">
        <div class="app-text">
            <h1 class="h1-mega">Job Tracker App</h1>
            <p class="p-large">
                Contrary to popular belief, Lorem Ipsum is not simply random
                text. It has roots in a piece of classical Latin literature from
                45 BC, making it over 2000 years old. Richard McClintock, a
                Latin professor at Hampden-Sydney College in Virginia, looked up
                one of the more obscure Latin words, consectetur, from a Lorem
                Ipsum passage, and going through the cites of the word in
                classical literature, discovered the undoubtable source. Lorem
                Ipsum comes from sections 1.10.32 and 1.10.33 of "de Finibus
                Bonorum et Malorum" (The Extremes of Good and Evil) by Cicero,
                written in 45 BC. This book is a treatise on the theory of
                ethics, very popular during the Renaissance. The first line of
                Lorem Ipsum, "Lorem ipsum dolor sit amet..", comes from a line
                in section 1.10.32. The standard chunk of Lorem Ipsum used since
                the 1500s is reproduced below for those interested. Sections
                1.10.32 and 1.10.33 from "de Finibus Bonorum et Malorum" by
                Cicero are also reproduced in their exact original form,
                accompanied by English versions from the 1914 translation by H.
                Rackham.
            </p>
        </div>
    </div>
    <div class="screens">
        <div class="live-demo">
            <iframe
                title="live demo"
                src="http://localhost:3000"
                height="812px"
                width="375px"
                style="border-radius:40px"
                class="responsive-iframe"
            />
        </div>
        <div class="all-screens">
            {#each [1, 2, 3, 4, 5, 6, 7, 1] as imgNum}
                <img src={`/figma/job/flat${imgNum}.png`} alt="group" />
            {/each}
        </div>
    </div>
</div>

<style>
    .all-screens::-webkit-scrollbar {
        width: 5px;
        height: 8px;
        background-color: #aaa; /* or add it to the track */
    }

    .app-desc {
        display: flex;
    }

    .app-text {
        margin-right: 40px;
    }

    .main-app {
        padding: 40px;
    }

    .all-screens {
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        row-gap: 20px;
        column-gap: 20px;
    }

    .screens {
        display: flex;
        justify-content: space-evenly;
    }

    .all-screens img {
        width: 14vw;
        margin-right: 30px;
    }

    .h1-mega {
        font-size: 4vw;
        margin: 0;
        font-family: "PT Sans Narrow", sans-serif;
        padding-bottom: 30px;
        display: inline-block;
        border-bottom: 5px solid black;
    }

    .p-large {
        font-size: 1.5vw;
        font-family: "Bebas Neue", cursive;
        text-align: justify;
    }

    .live-demo {
        overflow: hidden;
    }

    .responsive-iframe::-webkit-scrollbar {
        width: 5px;
        height: 5px;
    }

    /* Track */

    .responsive-iframe::-webkit-scrollbar-track {
        background: #f1f1f1;
        border-radius: 10px;
    }

    /* Handle */

    .responsive-iframe::-webkit-scrollbar-thumb {
        background: #888;
    }

    /* Handle on hover */

    .responsive-iframe::-webkit-scrollbar-thumb:hover {
        background: #555;
    }

    @media (max-width: 780px) {
        .all-screens {
            display: block;
        }

        .all-screens img {
            display: block;
            width: 100vw;
        }

        .app-desc {
            flex-direction: column;
        }

        .app-text {
            margin-right: 0;
        }

        .main-app {
            padding: 0;
        }

        .live-demo {
            display: none;
        }
    }

    @media screen and (min-width: 1025px) and (max-width: 1280px) {
        .app-desc {
            flex-direction: column;
        }

        .screens {
            flex-direction: column;
            align-items: center;
        }

        .all-screens {
            max-width: 100vw;
        }

        .all-screens img {
            width: 20vw;
            margin-right: 0;
        }

        .responsive-iframe {
            width: 345px;
            height: 630px;
            border-radius: 10px;
        }
    }
</style>
