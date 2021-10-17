<div id="banner-content">
    <h1 class="h1-mega">Hello</h1>
    <h1 class="h1-mega">I'm John Doe</h1>
    <p class="p-large">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
        veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
        commodo consequat. Duis aute irure dolor in reprehenderit in voluptate
        velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint
        occaecat cupidatat non proident, sunt in culpa qui officia deserunt
        mollit anim id est laborum.
    </p>
    <div class="icon-container">
        <i class="bx bxl-linkedin-square bx-lg" />
        <i class="bx bxl-github bx-lg" />
        <i class="bx bxl-google bx-lg" />
        <i class="bx bxl-behance bx-lg" />
    </div>
</div>

<style>
    #banner-content {
        padding: 8% 5%;
        flex: 0.4;
    }

    .h1-mega {
        font-size: 4vw;
        margin: 0;
        font-family: "PT Sans Narrow", sans-serif;
    }

    .p-large {
        font-size: 1.5vw;
        font-family: "Bebas Neue", cursive;
        text-align: justify;
    }

    .icon-container i {
        margin-right: 20px;
        padding: 5px;
        border-radius: 5px;
        background: #151515;
    }

    .icon-container {
        display: flex;
    }

    @media (max-width: 780px) {
        .h1-mega {
            font-size: 36px;
            padding-bottom: 10px;
        }
        .p-large {
            font-size: 18px;
        }
        .icon-container {
            justify-content: space-between;
        }

        .icon-container i {
            margin: 0;
        }
    }
</style>
