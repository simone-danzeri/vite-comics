<script>
import AppHeader from './components/AppHeader.vue';
import AppCards from './components/AppCards.vue';
import AppMainNav from './components/AppMainNav.vue';
import AppFooter from './components/AppFooter.vue';
import AppJumbotron from './components/AppJumbotron.vue';

  export default {
    components: {
      AppHeader,
      AppCards,
      AppMainNav,
      AppFooter,
      AppJumbotron
    },
  }
</script>


<template>
  <AppHeader></AppHeader>

  <main>
    <AppJumbotron></AppJumbotron>
    <AppCards></AppCards>
    <AppMainNav></AppMainNav>
  </main>

  <AppFooter></AppFooter>
</template>


<style lang="scss">
  @use './style/generic.scss'
</style>