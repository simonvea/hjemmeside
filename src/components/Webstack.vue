<template>
    <section class="tech">
        <section class="front-end">
            <h3>Frontend</h3>
            <div class="logos">
                <img src="../assets/logo.png">
                <img src="../assets/HTML5_Logo.svg">
                <img src="../assets/CSS3_logo_and_wordmark.svg">
                <img src="../assets/JavaScript-logo.png">
            </div>
        </section>
        <section class="back-end">
            <h3>Backend</h3>
            <div class="logos">
                <img src="../assets/Node.js_logo.svg">
                <img src="../assets/Firebase_Logo.png">
            </div>
        </section>
    </section>
</template>

<style scoped>

    .tech {
        background: #feffff;
        width: 80%;
        margin: 0 auto 10rem;
        padding: 5rem 2rem;
        border-radius: 3rem;
        box-shadow: 0 5px 40px #17252A;
        display: grid;
        grid-template-rows: 1fr 1fr;
        grid-template-columns: auto;
    }

    .front-end, .back-end {
        text-align: center;
        height: 100%;
        display: flex;
        justify-content: space-around;
        flex-direction: column;
    }

    .front-end {
        grid-row: 1;
    }

    .front-end .logos {
        border-bottom: 1px dashed #17252A;
        padding-bottom: 5vh;
    }

    .back-end {
        grid-row: 2;
    }

    h3 {
        margin-bottom: 5%;
    }

    .back-end h3 {
        margin-top: 5vh;
    }

    .logos {
        display: flex;
        justify-content: space-around;
        flex-wrap: wrap;
    }

    .back-end .logos {
        flex-direction: column;
    }

    .front-end img {
        height: 80px;
        margin-right: 10px;
        margin-top: 10px;
    }

    .back-end img {
        max-width: 100%;
        height: 60px;
        margin-right: 10px;
        margin-top: 30px;
    }


    /* -------------------------
    --- Tablets and desktops --- 
    ------------------------- */

    @media only screen and (min-width: 768px) {
        .tech {
            grid-template-columns: 1fr 1fr;
            grid-template-rows: auto;
        }

        .front-end {
            grid-column: 1;
            grid-row: 1;
        }

        .front-end .logos {
            border-right: 1px dashed #17252A;
            border-bottom: 0;
            padding-bottom: 0;
        }

        .back-end {
            grid-column: 2;
            grid-row: 1;
        }

        .back-end h3 {
            margin-top: 0;
        }

        .back-end .logos {
            flex-direction: row;
        }
    }
</style>

