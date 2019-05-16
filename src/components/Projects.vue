<template>
    <section class="projects-container">
            <h2>Et utvalg av hva jeg har laget</h2>
            <section class="projects">
                    <article class="project" v-for="(project, index) in projects" :key="index">
                        <section class="project-info">
                            <h3>{{project.name}}</h3>
                            <p> {{project.info}} </p>
                            <h4>Egenskaper:</h4>
                            <ul>
                                <li v-for="(egenskap, egenskapIndex) in project.egenskaper" :key="egenskapIndex">
                                    {{egenskap}}
                                    </li>
                            </ul>
                        </section>
                        <section class="project-view">
                            <div class="img">
                                <img :src="project.img" alt="Bilde av prosjektet">
                            </div>
                            <div class="links">
                                <a v-if="project.linkToPlay" v-bind:href="project.linkToPlay" target="_blank">Se side</a>
                                <a v-bind:href="project.linkToCode" target="_blank">Se kode</a>
                            </div>
                        </section>
                    </article>
            </section>
    </section>
</template>

<style scoped>
    .projects-container {
        margin-top: -5vh;
        width: 90%;
        margin: auto;
        color: #17252A;
        background-color: #feffff;
    }

    h2, h3 {
        text-align: center;
    }

    .project {
        display: grid;
        grid-template-rows: 50% 50%;
        border-radius: 2rem;
        margin: 2rem auto 4rem;
        padding: 2rem 2rem 2rem 2rem;
        box-shadow: 0 10px 10px #2B7A78;
    }

    .project-info {
        grid-row: 2;
    }

    h3 {
        margin: 1rem 0;
    }

    p {
        margin-bottom: 1rem;
    }

    ul {
        margin-top: 0.5rem;
        margin-left: 2em;
    }

    li {
        margin: 5px 0;
    }

    .project-view {
        grid-row: 1;
        display: flex;
        flex-direction: column;
        justify-content: center;
    }

    .project-view .img {
        margin-bottom: 20px;
        display: flex;
        justify-content: center;
    }

    img {
        border-radius: 5px;
        max-width: calc(324px - 4rem);
        max-height: 141px;
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
        padding: 4px 9px;
        /* cursor: pointer; */
    }

/* ---------------------------------
-------Tablet and desktop-----------
--------------------------------- */

@media only screen and (min-width: 768px) {
    .projects-container {
        width: 85%;
        max-width: 850px;
    }

    .project {
        grid-template-columns: 50% 50%;
        grid-template-rows: auto;
        padding: 2rem 2rem 2rem 4rem;
    }

    .project-info {
        grid-column: 1;
        grid-row: 1;
    }

    
    .project-view {
        grid-column: 2;
    }

    @media only screen and (min-width: 1281px) {
        img {
            max-width: calc(500px - 4rem);
            max-height: 200px;
        }
    }

}


</style>

<script>
//For å kunne bruke bilder fra assets
const kalkulatorImg = require('../assets/prosjekt-kalkulator.png')
const hjemmesideImg = require('../assets/hjemmeside.png')
const pizzaImg = require('../assets/pizza-sjappe.png')

export default {
    data() {
        return {
            projects: [
                {
                    name: "Pizzahuset",
                    info: "En fiktiv nettside for en pizzasjappe. Nettsiden inkluderer en adminside som dynamisk endrer menyen og behandler bestillinger.",
                    egenskaper: [
                        "Single Page Application (Vue.js/Vue Router)",
                        "Brukerautentisering (Firebase)",
                        "Interaktiv database (Firebase)",
                        "Handlekurv (Vuex/Firebase)",
                        "Bootstrap"
                    ],
                    linkToPlay: "https://simonvea.github.io/pizzahuset",
                    linkToCode: "https://github.com/simonvea/pizzahuset",
                    img: pizzaImg
                },
                {
                    name: "Kalkulator",
                    info: "En kalkulator laget i vanilla JavaScript og HTML/CSS.",
                    egenskaper: [
                        "Ingen rammeverk",
                        "JavaScript DOM manipulering"
                    ],
                    linkToPlay: "https://simonvea.github.io/kalkulator/",
                    linkToCode: "https://github.com/simonvea/kalkulator",
                    img: kalkulatorImg
                },
                {
                    name: "simonopheim.no",
                    info: "Min landings-side.",
                    egenskaper: [
                        "Lazy loading og kodestruktur gjennom Vue.js",
                        "Mobile-first responsive design",
                        "Distribuert gjennom Netlify"
                    ],
                    linkToCode: "https://github.com/simonvea/hjemmeside",
                    img: hjemmesideImg
                }
            ]
        }
    }
}
</script>

