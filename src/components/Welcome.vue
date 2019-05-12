<template>
    <section class="welcome">
            <h1>Simon Opheim</h1>
            <!-- <h2>Master i filosofi &amp; Webutikler</h2> -->
            <h2>{{techSkills[index]}}</h2>
            <h3>
                Jeg er en selvlært webutikler.
                Jeg liker å lage webapplikasjoner som hjelper oss leve bedre liv.
            </h3>
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
    }

    h3 {
        border-top: 1px solid #DEF2F1;
        padding-top: 1px;
        width: 350px;
        text-align: center;
    }
</style>

<script>
import { setInterval } from 'timers';
export default {
    data() {
        return {
            titles: ["Master i filosofi", "Webutvikler", "Medieanalytiker"],
            techSkills: ["Javascript ES6", "HTML5", "CSS3", "Vue.js", "Vuex", "Firebase"],
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
            }, 1500)
        }
    },
    beforeMount() {
        this.alternateSkills()
    }
}
</script>
