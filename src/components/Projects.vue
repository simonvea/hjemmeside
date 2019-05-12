<template>
    <section class="projects-container">
            <h2>Hva jeg har laget</h2>
            <section class="projects">
                <article class="project" v-for="(project, index) in projects" :key="index">
                    <section class="project-info">
                        <h3>{{project.name}}</h3>
                        <p> {{project.info}} </p>
                        <h4>Egenskaper:</h4>
                        <ul v-for="(egenskap, index) in project.egenskaper" :key="index">
                            <li>{{egenskap}}</li>
                        </ul>
                    </section>
                    <section class="project-view">
                        <div class="img">
                            <img :src="project.img">
                        </div>
                        <div class="links">
                            <a v-bind:href="project.linkToPlay">Se side</a>
                            <a v-bind:href="project.linkToCode">Se kode</a>
                        </div>
                    </section>
                </article>
            </section>
    </section>
</template>

<style scoped>
    .projects-container {
        margin-top: -5vh;
        width: 75%;
        margin: auto;
        color: #17252A;
        background-color: #feffff;
    }

    h2, h3 {
        text-align: center;
    }

    .project {
        display: grid;
        grid-template-columns: 50% 50%;
        border-radius: 2rem;
        margin: 2rem auto 4rem;
        padding: 2rem 2rem 2rem 4rem;
        box-shadow: 0 10px 10px #2B7A78;
    }

    .project-info {
        grid-column: 1;
    }

    h3 {
        margin-bottom: 2rem;
    }

    p {
        margin-bottom: 1rem;
    }

    ul {
        margin-top: 0.5rem;
        margin-left: 2em;
    }

    .project-view {
        grid-column: 2;
    }

    .project-view .img {
        max-width: 70%;
        height: 30vh;
        margin: auto;
        margin-bottom: 20px;
        display: flex;
        justify-content: center;
    }

    img {
        max-height: 100%;
        border-radius: 5px;
    }

    .links {
        display: flex;
        justify-content: center;
    }

    a {
        display: block;
        text-align: center;
        padding: 5px 10px;
        text-decoration: none;
        background-color: #2B7A78;
        color: #DEF2F1;
        font-size: 2vh;
        border-radius: 5px;
        margin: 0 10px;
        /* border-left: 0.5px solid #DEF2F1;
        border-bottom: 0.5px solid #DEF2F1; */
    }

    a:hover {
        background-color: #DEF2F1;
        color: #17252A;
        border: 0.5px solid #2B7A78;
        /* cursor: pointer; */
    }
</style>

<script>
//For å kunne bruke bilder fra assets
const kalkulatorImg = require('../assets/prosjekt-kalkulator.png')

export default {
    data() {
        return {
            projects: [
                {
                    name: "Kalkulator",
                    info: "En kalkulator laget i vanilla Javascript og HTML/CSS.",
                    egenskaper: [
                        "interaktiv",
                        "Javascript DOM manipulering"
                    ],
                    linkToPlay: "https://simonvea.github.io/prosjekter/Calculator/",
                    linkToCode: "url2",
                    img: kalkulatorImg
                },
                {
                    name: "Pizza planet",
                    info: "En fiktiv nettside for en pizzasjappe. Nettsiden inkluderer en adminside som dynamisk endrer menyen og leser bestillinger. Laget ved bruk av Vue.js Vuex og firestore.",
                    egenskaper: [
                        "interaktiv",
                        "Vue.js"
                    ],
                    linkToPlay: "url1",
                    linkToCode: "url2",
                    img: "img-url" 
                },
                {
                    name: "Hjemmeside",
                    info: "test",
                    egenskaper: [
                        "Test",
                        "Javascript DOM manipulering"
                    ],
                    linkToPlay: "url1",
                    linkToCode: "url2",
                    img: "img-url" 
                }
            ]
        }
    }
}
</script>

