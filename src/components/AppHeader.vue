<template>
    <div class="header-top">
        <span>everything about lifestyle, travel and gadgets</span>
        <!-- dinamici -->
        <ul>
            <li>sign in</li>
            <li>about us</li>
            <li>contact us</li>
            <li>buy now</li>
        </ul>
    </div>
    <div class="header-logo">
        <img src="../assets/logo-default-slim.png" alt="logo">
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
    @include mixins.d-flex-align-center;
    height: 50px;

    ul {
        @include mixins.d-flex-align-center;
        list-style: none;
        padding: 0px 20px;

        li {
            padding: 0px 10px;
        }
    }
}
</style>