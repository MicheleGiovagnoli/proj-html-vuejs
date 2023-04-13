<template>
    <div class="blueBar">
        <div class="container">
            <div class="box">
                <i class="fa-solid fa-chevron-left"></i>
                <span v-for="(element, i ) in blueBar">{{ element }}</span>
                <i class="fa-solid fa-chevron-right"></i>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    nome: 'AppBlueBar',
    props: {
        blueBar: Array,
    }
}
</script>
<style lang="scss">
@use '../styles/partials/variables' as*;
@use '../styles/partials/mixins';
@use '../styles/general.scss';

.blueBar {
    background-color: $color-primary;

    .container {
        display: flex;
        align-items: center;
        justify-content: center;
        padding: 30px 0px;
        @include mixins.center;

        .box {
            display: flex;
            justify-content: space-between;
            align-items: center;
            width: 100%;

            span {
                background-color: $color-background-6;
                color: $color-white;
                padding: 15px 50px;
                margin: 0px 15px;
                font-size: 10px;
                font-weight: bolder;

            }
        }
    }
}
</style>