<script>
import AppHeader from './components/AppHeader.vue';
import AppCards from './components/AppCards.vue';
import AppMainNav from './components/AppMainNav.vue';
import AppFooter from './components/AppFooter.vue';

  export default {
    components: {
      AppHeader,
      AppCards,
      AppMainNav,
      AppFooter
    },
  }
</script>


<template>
  <AppHeader></AppHeader>

  <main>
    <AppCards></AppCards>
    <AppMainNav></AppMainNav>
  </main>

  <AppFooter></AppFooter>
</template>


<style lang="scss">
  @use './style/generic.scss'
</style>