<template>
  <div class="wrapper">
    <AppHeader />
    <AppMain />
  </div>
</template>
<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
export default {
  components: {
    AppHeader,
    AppMain,
  },
  data() {
    return {
      preview: ["../assets/blog-46", "../assets/blog-47", "../assets/blog-48", "../assets/blog-49", "../assets/blog-50", "../assets/blog-51"]
    }
  }
}
</script>
<style lang="scss">
@use './styles/general.scss';
</style>