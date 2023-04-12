<template>
    <div class="main">
        <!-- Passare i dati attraverso le props e generare 'carte' -->
        <AppPreview />
    </div>
</template>
<script>
import AppPreview from './AppPreview.vue';
export default {
    nome: 'AppMain',
    components: {
        AppPreview,
    }
}
</script>
<style lang="scss">
@use '../styles/partials/variables' as*;
@use '../styles/partials/mixins';
</style>