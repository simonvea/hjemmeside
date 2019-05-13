<template>
    <section class="about">
        <div class="container">
            <h2>Hei, jeg heter Simon.</h2>
            <p> 
                Webutvikling er  <em> gøy</em>. 
            </p>
            <p> Derfor har jeg endt opp med å lære meg webutvikling på egenhånd. </p>
            <p> Jeg er nå på utkikk etter andre som deler min interesse for programmering og som liker å bygge kule ting på nett. </p>
            
            <p>
                Fra å leke med html og Microsoft Frontpage på ungdomskolen, 
                så har jeg etter flere års studier i filosofi (master), samfunnsøkonomi (bachelor), sosialt entreprenørskap og ingeniørstudier, 
                endelig funnet tilbake til det jeg virkelig elsker: webutvikling.
            </p>
            <p>
                Til daglig jobber jeg som medieanalytiker, men på ettermiddagen og mens jeg sover så koder jeg. Jeg elsker å lære nye ting og prøver dem ofte ut i søvne. 
                Noen koder &quot;HelloWorld&quot;. Jeg koder drømmene mine.
            </p>
            <p>
                Så langt så har jeg laget nettsider, script og apper ved bruk av blant annet: 
            </p>
            <p> 
                HTML5, CSS3, JavaScript ES6, Git, Vue.js, Vuex, Firebase, Google Apps Scripts, Ruby og Python.
            </p>
            <a href="https://github.com/simonvea" target="_blank" id="github"><img src="../assets/GitHub-Mark-32px.png" alt="GitHub mark"></a>
            <p>
                Om du er ute etter hjelp til å lage noe ved bruk av denne type verktøy, så <a href="#kontakt">ta gjerne kontakt</a>. 
            </p>
            <p>
                Du vil møte en som elsker å lære nye ting og som er veldig interessert i å begynne å jobbe med utvikling på fulltid.
            </p>
        </div>
    </section>
</template>

<style scoped>

    .about {
        padding: 13rem 3rem 14rem;
        text-align: center;
        margin-bottom: -9rem;
        background-color: #2B7A78;
        color: #DEF2F1;
    }

    .container {
        width: 100%;
        margin: auto;
    }

    h2 {
        margin-bottom: 5vh;
    }

    p {
        margin: 2vh 5px;
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
    }


</style>

