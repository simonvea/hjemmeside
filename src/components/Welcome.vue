<template>
    <section class="welcome">
            <h1>Simon Opheim</h1>
            <!-- <h2>Master i filosofi &amp; Webutikler</h2> -->
            <h2>{{titles[index]}}</h2>
            <h3>
                Jeg er en selvlært webutikler.
                Jeg liker å lage webapplikasjoner som hjelper oss leve bedre liv.
            </h3>
    </section>
</template>

<style scoped>
    .welcome {
        height: 90vh;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        text-align: center;
        color: #DEF2F1;
        background-image: linear-gradient(rgb(43, 122, 120, 0.6), rgb(58, 175, 169)), url("../assets/sauda.jpg");
        background-size: cover;
        background-position: 50%;
        background-repeat: no-repeat;
    }

    h1 {
        text-transform: uppercase;
        font-weight: 600;
    }

    h2 {
        padding: 0 3rem;
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
            index: 0
        }
    },
    methods: {
        changeTitle: function () {
            setInterval(() => {
                if(this.index < this.titles.length-1){
                    this.index++
                } else {
                    this.index=0;
                }
            }, 1500)
        }
    },
    beforeMount() {
        this.changeTitle()
    }
}
</script>
