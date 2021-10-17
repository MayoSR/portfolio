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
</script>

<div id="box-container">
    <div id="skill-box">
        {#each icons as icon}
            <div class="skill-box">
                <img src={icon.url} class="skill-icons" alt={icon.name} />
            </div>
        {/each}
    </div>
</div>

<style>
    #box-container {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 100%;
        overflow: hidden;
        flex: 0.6;
        display: none;
    }
    .skill-box img {
        height: 40px;
        width: 40px;
        padding: 10px;
    }

    #skill-box {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr 1fr;
        padding: 20px;
        text-align: center;
    }
    @media (max-width: 780px) {
        #box-container {
            display: block;
        }
    }
</style>
