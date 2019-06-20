<template>
    <article class="info-card" data-aos="flip-up" :data-aos-delay="delay">
        <h3 class="card-header">{{ title }}</h3>
        <p class="card-paragraph"> {{ textContent }} </p>
    </article>
</template>

<script>
export default {
    name: "card",
    props: ["title", "textContent", "delay"]
}
</script>

<style>
    .info-card {
        border-radius: 2rem;
        margin: 1rem;
        padding: 2rem 2rem 2rem 2rem;
        box-shadow: 0 5px 5px #17252A;
        text-align: center;
        width: 300px;
        background-color: rgb(58, 175, 169);
        color:#17252A;
    }

    .card-paragraph {
        margin-top: 1rem;
    }
</style>
