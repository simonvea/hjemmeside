<template>
    <section class="about">
        <div class="container">
            <h2>Hei, jeg heter Simon.</h2>
            <p> Jeg digger å løse problemer. </p>
        </div>
        <section class="cards-container">
            <card
                v-for="(card, index) of cardsContents" v-bind:key="index"
                v-bind:title="card.title"
                v-bind:textContent="card.content"
                v-bind:delay="addDelayOnBigScreen(index)"
            ></card>
        </section>
        <div class="container">
        
            <p>
                Så langt så har jeg laget nettsider, script og apper ved bruk av blant annet: 
            </p>
            <p> 
                HTML5, CSS3, JavaScript ES6, Git, React, Vue.js, Vuex, Firebase, Node.js, Express, MongoDB, Ruby, Python og Google Apps Scripts.
            </p>
            <a href="https://github.com/simonvea" target="_blank" id="github"><img src="../assets/GitHub-Mark-32px.png" alt="GitHub mark"></a>
            <p>
                Om du er ute etter hjelp til å lage noe ved bruk av denne type verktøy, så <a href="#kontakt">ta gjerne kontakt</a>. 
            </p>
        </div>
    </section>
</template>

<script>
import card from "./Card.vue"

export default {
    data() {
        return {
            cardsContents: [
                {
                    title: "Build",
                    content: "Min kompetanse innen webutvikling gjør at jeg utvikler løsningen kunden, og du, trenger."
                },
                {
                    title: "Measure",
                    content: "Min erfaring fra Lean startup og sosialt entreprenørskap gjør at jeg effektivt og kontinuerlig identifiserer en løsning."
                },
                {
                    title: "Learn",
                    content: "Min mastergrad innen filosofi har gjort meg til en god lytter og kommunikator. Dette gjør at jeg raskt tilegner meg den riktige lærdomen og kommuniserer den effektivt videre."
                }
            ],
        }
    },
    components: {
        card,
    },
    methods: {
        addDelay(number) {
            const delayMs = 300;
            return delayMs * number
        },
        addDelayOnBigScreen(number) {
            const minScreenSize = 768;
            if (window.innerWidth > minScreenSize) {
                return this.addDelay(number)
            }
            return 0
        }
    }
}
</script>


<style scoped>

    .about {
        padding: 13rem 0 14rem;
        text-align: center;
        margin-bottom: -9rem;
        background-color: #2B7A78;
        color: #DEF2F1;
    }

    .container {
        width: 100%;
        margin: auto;
    }

    .cards-container {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: space-around;
        width: 100%;
    }

    h2 {
        margin-bottom: 5vh;
    }

    p {
        margin: 2vh 3rem;
    }

    #github:hover {
        content: url("../assets/GitHub-Mark-Light-32px.png");
    }

    a {
        text-decoration-color: #17252A;
        color: #17252A;
    }

    

    @media only screen and (min-width: 768px) {
        .container {
            width: 80%;
        }

        p {
            margin: 2vh;
        }

        .cards-container {
            flex-direction: row;
            align-items: initial;
        }
    }


</style>

