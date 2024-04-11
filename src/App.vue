<script>
import AppHeader from './components/AppHeader.vue';
import AppCards from './components/AppCards.vue';
import AppMainNav from './components/AppMainNav.vue';

  export default {
    components: {
      AppHeader,
      AppCards,
      AppMainNav
    }
  }
</script>


<template>
  <AppHeader></AppHeader>

  <main>
    <AppCards></AppCards>
    <AppMainNav></AppMainNav>
  </main>
</template>


<style lang="scss">
  @use './style/generic.scss'
</style>