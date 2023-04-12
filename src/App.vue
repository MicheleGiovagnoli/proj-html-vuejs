<template>
  <div class="wrapper">
    <AppHeader />
  </div>
</template>
<script>
import AppHeader from './components/AppHeader.vue'
export default {
  components: {
    AppHeader,
  }
}
</script>
<style lang="scss">
@use './styles/general.scss';

.wrapper {
  width: 80%;
  margin: auto;
}
</style>