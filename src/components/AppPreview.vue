<template>
    <!-- Creare la struttura dati e renderli dinamici -->
    <div class="preview">
        <div class="container">
            <div class="card">
                <img src="../assets/blog-46.jpg" alt="img">
                <div class="info">
                    <button class="button-primary">photography</button>
                    <h1>How to take better concert pictures in 30 Seconds</h1>
                </div>
            </div>
            <div class="card">
                <img src="../assets/blog-47.jpg" alt="img">
                <div class="info">
                    <button class="button-primary">photography</button>
                    <h1>How to take better concert pictures in 30 Seconds</h1>
                </div>
            </div>
            <div class="card">
                <img src="../assets/blog-48.jpg" alt="img">
                <div class="info">
                    <button class="button-primary">photography</button>
                    <h1>How to take better concert pictures in 30 Seconds</h1>
                </div>
            </div>
            <div class="card">
                <img src="../assets/blog-49.jpg" alt="img">
                <div class="info">
                    <button class="button-primary">photography</button>
                    <h1>How to take better concert pictures in 30 Seconds</h1>
                </div>
            </div>
            <div class="card">
                <img src="../assets/blog-50.jpg" alt="img">
                <div class="info">
                    <button class="button-primary">photography</button>
                    <h1>How to take better concert pictures in 30 Seconds</h1>
                </div>
            </div>
            <div class="card">
                <img src="../assets/blog-51.jpg" alt="img">
                <div class="info">
                    <button class="button-primary">photography</button>
                    <h1>How to take better concert pictures in 30 Seconds</h1>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    nome: 'AppPreview',
}
</script>
<style lang="scss">
@use '../styles/partials/variables' as*;
@use '../styles/partials/mixins';
@use '../styles/general.scss';

.preview {
    background-color: $color-background-1;

    .container {
        @include mixins.center;
        display: flex;
        flex-wrap: wrap;

        img {
            padding: 10px;
            width: 100%;
        }

        .card {
            position: relative;
            width: calc(100% / 3);


            .info {
                width: 90%;
                color: white;
                font-size: 10px;
                position: absolute;
                bottom: 30px;
                left: 30px;

                button {
                    margin-bottom: 20px;
                }
            }
        }
    }
}
</style>