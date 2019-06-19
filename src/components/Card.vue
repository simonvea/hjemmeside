<template>
    <article class="info-card">
        <h3 class="card-header">{{ title }}</h3>
        <p class="card-paragraph"> {{ textContent }} </p>
    </article>
</template>

<script>
export default {
    name: "card",
    props: ["title", "textContent"]
}
</script>

<style>
    .info-card {
        border-radius: 2rem;
        margin: 1rem;
        padding: 2rem 2rem 2rem 2rem;
        box-shadow: 0 10px 10px #17252A;
        text-align: center;
        width: 300px;
    }

    .card-paragraph {
        margin-top: 1rem;
    }
</style>
