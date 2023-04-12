<template>
    <div class="header">
        <div class="header-top">
            <div class="container">
                <span>everything about lifestyle, travel and gadgets</span>
                <!-- Creare struttura dati e Rendere Dinamici  -->
                <ul>
                    <li>SIGN IN</li>
                    <li>ABOUT US</li>
                    <li>CONTACT US</li>
                    <li>BUY NOW</li>
                </ul>
            </div>
        </div>
        <div class="header-logo">
            <div class="container">
                <img src="../assets/logo-default-slim.png" alt="logo">
            </div>
        </div>
        <div class="header-bottom">
            <div class="container">
                <!-- Creare struttura dati e Rendere Dinamici -->
                <ul>
                    <li>HOME</li>
                    <li>ELEMENTS</li>
                    <li>FEATURES</li>
                    <li>PAGES</li>
                    <li>PORTFOLIO</li>
                    <li>BLOG</li>
                    <li>SHOP</li>
                </ul>
                <i class="fa-solid fa-magnifying-glass"></i>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    nome: 'AppHeader',
}
</script>
<style lang="scss">
@use '../styles/partials/variables' as*;
@use '../styles/partials/mixins';

.header-top {
    background-color: $color-primary;

    .container {
        @include mixins.d-flex-align-center;
        @include mixins.center;
        height: 50px;
        font-size: 12px;

        ul {
            @include mixins.d-flex-align-center;
            list-style: none;
            padding: 0px 20px;

            li {
                padding: 0px 10px;
            }
        }
    }
}

.header-logo {
    background-color: $color-white;
    border-bottom: 2px solid $color-border-3;

    .container {
        @include mixins.d-flex-align-center;
        @include mixins.center;
        height: 100px;

        img {
            width: 100px;
        }
    }
}

.header-bottom {
    background-color: $color-white;
    border-bottom: 2px solid $color-border-3;

    .container {
        @include mixins.d-flex-align-center-space-between;
        @include mixins.center;
        height: 50px;

        ul {
            @include mixins.d-flex-align-center;
            list-style: none;

            li {
                padding-right: 10px;
                font-weight: bold;
                color: $color-text-5;
            }
        }
    }
}
</style>