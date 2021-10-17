<script>
    import { onMount } from "svelte";

    let icons = [
        {
            url: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg",
            name: "MySQL",
        },
        {
            url: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/firebase/firebase-plain.svg",
            name: "Firebase",
        },
        {
            url: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nextjs/nextjs-original.svg",
            name: "NextJs",
        },
        {
            url: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/redux/redux-original.svg",
            name: "Redux",
        },
        {
            url: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg",
            name: "Git",
        },
        {
            url: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jenkins/jenkins-original.svg",
            name: "Jenkins",
        },
        {
            url: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/socketio/socketio-original.svg",
            name: "SocketIO",
        },
        {
            url: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mongodb/mongodb-original.svg",
            name: "MongoDB",
        },
        {
            url: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/kubernetes/kubernetes-plain.svg",
            name: "Kubernetes",
        },
        {
            url: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg",
            name: "Docker",
        },
        {
            url: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/angularjs/angularjs-original.svg",
            name: "Angular",
        },
        {
            url: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg",
            name: "React",
        },
        {
            url: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/php/php-original.svg",
            name: "PHP",
        },
        {
            url: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/c/c-original.svg",
            name: "C/C++",
        },
        {
            url: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg",
            name: "NodeJs",
        },
        {
            url: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg",
            name: "JavaScript (ES6+)",
        },
        {
            url: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg",
            name: "Python",
        },
        {
            url: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg",
            name: "Java",
        },
        {
            url: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tensorflow/tensorflow-original.svg",
            name: "Tensorflow",
        },
        {
            url: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bootstrap/bootstrap-original.svg",
            name: "Bootstrap",
        },
        {
            url: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/materialui/materialui-original.svg",
            name: "Material UI",
        },
        {
            url: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/figma/figma-original.svg",
            name: "Figma",
        },
        {
            url: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jquery/jquery-original.svg",
            name: "jQuery",
        },
        {
            url: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linux/linux-original.svg",
            name: "Linux",
        },
        {
            url: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/svelte/svelte-original.svg",
            name: "Svelte",
        },
        {
            url: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/express/express-original.svg",
            name: "Express",
        },
        {
            url: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/flask/flask-original.svg",
            name: "Flask",
        },
        {
            url: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/graphql/graphql-plain.svg",
            name: "GraphQL",
        },
        {
            url: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/spring/spring-original.svg",
            name: "Spring",
        },
        {
            url: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/raspberrypi/raspberrypi-original.svg",
            name: "Raspberry Pi",
        },
    ];

    onMount(() => {
        let imgSize = 50;
        let iconList = document.getElementsByClassName("icon-box");
        let iconLength = iconList.length;
        console.log(iconLength);
        let radius = Math.floor(
            document.getElementById("skill-wheel").offsetWidth / 2
        );
        let theta = Math.floor(360 / iconLength);

        for (let i = 0; i < iconList.length; i++) {
            iconList[i].style.height = imgSize + "px";
            iconList[i].style.width = imgSize + "px";
            iconList[i].style.top =
                radius -
                imgSize / 2 +
                radius * Math.cos((i * Math.PI * theta) / 180) +
                "px";
            iconList[i].style.left =
                radius -
                imgSize / 2 +
                radius * Math.sin((i * Math.PI * theta) / 180) +
                "px";
        }
    });

    var timeOut = null;
    function displayIconName(e, name) {
        clearTimeout(timeOut);
        if (e.type === "mouseenter")
            document.getElementById("icon-name").textContent = name;
        else {
            timeOut = setTimeout(() => {
                document.getElementById("icon-name").textContent =
                    "Don't recognize an icon? Hover on it!";
            }, 2000);
        }
    }
</script>

<div id="skill-container">
    <div id="skill-wheel">
        <div id="my-skills">
            <h1 class="h1-mega" style="text-align:center">My Skills</h1>
            <p class="p-large" id="icon-name">
                Don't recognize an icon? Hover on it!
            </p>
        </div>
        {#each icons as icon}
            <div class="icon-box">
                <img
                    src={icon.url}
                    class="skill-icons"
                    on:focus={(e) => displayIconName(e, icon.name)}
                    on:mouseenter={(e) => displayIconName(e, icon.name)}
                    on:mouseleave={(e) => displayIconName(e, icon.name)}
                    alt={icon.name}
                />
            </div>
        {/each}
    </div>
</div>

<style>
    #skill-container {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 100%;
        overflow: hidden;
        flex: 0.6;
    }

    #skill-wheel {
        border-radius: 50%;
        position: relative;
        width: 30vw;
        height: 30vw;
        animation: rotateCircle 60s infinite linear;
    }

    .icon-box {
        position: relative;
    }

    #skill-wheel > .icon-box {
        position: absolute;
        transition: ease all;
        animation: rotateCircle 60s infinite linear reverse;
        cursor: pointer;
    }

    @keyframes rotateCircle {
        from {
            transform: rotate(0deg);
        }

        to {
            transform: rotate(360deg);
        }
    }

    #my-skills {
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        width: 100%;
        height: 100%;
        position: absolute;
        display: flex;
        justify-content: center;
        align-items: center;
        animation: rotateCircle 60s infinite linear;
        animation-direction: reverse;
        flex-direction: column;
    }

    .p-large {
        font-size: 32px;
        font-family: "Bebas Neue", cursive;
    }

    .h1-mega {
        font-size: 72px;
        margin: 0;
        font-family: "PT Sans Narrow", sans-serif;
    }
    @media (max-width: 780px) {
        #skill-container {
            display: none;
        }
    }
</style>
