<template>
    <section class="welcome">
        <div class="container">
            <h1>Simon Opheim</h1>
            <!-- <h2>Master i filosofi &amp; Webutikler</h2> -->
            <h2>
                {{techSkills[index]}}
            </h2>
        </div>
            <h3>
                Jeg er en webutvikler.<br>Jeg lager kule nettapplikasjoner.
            </h3>
            <!-- <h4>
                <a href="#kontakt">Hyr meg</a> for å bygge <em>ditt</em> produkt.
            </h4> -->
    </section>
</template>

<style scoped>
    .welcome {
        height: 100vh;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        text-align: center;
        color: #DEF2F1;
        background-image: linear-gradient(rgb(58, 175, 169, 0.8), rgb(43, 122, 120)), url("../assets/sauda.jpg");
        background-size: cover;
        background-position: 50%;
        background-repeat: no-repeat;
        /* background-attachment: fixed; */
    }

    h1 {
        text-transform: uppercase;
        font-weight: 600;
    }

    h2 {
        padding: 0 3rem;
        margin-bottom: 5px;
        will-change: transform;
    }

    .container {
        width: 260px;
        border-bottom: 1px solid #DEF2F1;
    }

    h3 {
        padding-top: 5px;
        width: 350px;
        text-align: center;
    }

    h4 {
        margin-top: 5px;
    }

    a {
        color: #17252A;
        text-decoration-color: #17252A;
    }

    em {
        font-size: 1.2em;
    }
</style>

<script>
import { setInterval } from 'timers';
export default {
    data() {
        return {
            techSkills: ["Javascript", "HTML5", "CSS3", "Vue.js", "Vuex", "React", "Redux", "Firebase", "Node.js", "Express", "MongoDB"],
            index: 0
        }
    },
    methods: {
        alternateSkills: function () {
            setInterval(() => {
                if(this.index < this.techSkills.length-1){
                    this.index++
                } else {
                    this.index=0;
                }
            }, 1000)
        }
    },
    beforeMount() {
        this.alternateSkills()
    }
}
</script>
