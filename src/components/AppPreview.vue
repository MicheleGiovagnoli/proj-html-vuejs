<template>
    <!-- Creare la struttura dati e renderli dinamici -->
    <div class="card">
        <img :src="getImagePath(images)" :alt="images">
        <div class="info">
            <button class="button-primary">{{ types }}</button>
            <h1>{{ title }}</h1>
        </div>
    </div>
</template>
<script>
export default {
    nome: "AppPreview",
    props: {
        types: String,
        images: String,
        title: String,
    },
    methods: {
        getImagePath: function (img) {
            return new URL(`../assets/${img}`, import.meta.url).href;
        }
    },
}
</script>
<style lang="scss" scoped>
@use '../styles/partials/variables' as*;
@use '../styles/partials/mixins';
@use '../styles/general.scss';

.card {
    position: relative;
    width: calc(100% / 3);

    img {
        width: 97%;
    }

    .info {
        width: 80%;
        color: white;
        font-size: 40%;
        position: absolute;
        bottom: 10%;
        left: 10%;

        button {
            margin-bottom: 20px;
        }
    }
}
</style>