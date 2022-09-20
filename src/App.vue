<template>
  <header>
    <the-header></the-header>
  </header>
  <main>
    <RouterView />
  </main>
  <footer>
    <the-footer></the-footer>
  </footer>
</template>


<script lang="ts">
  import TheHeader from './components/TheHeader.vue'
  import TheFooter from './components/TheFooter.vue'

  export default {
    name: 'App',
    components: {
      TheHeader,
      TheFooter
    }
  }
</script>

<style scoped lang="scss">
  #app {
    background: var(--ui-color-light-gray);
    font-weight: normal;
    margin: 0 auto;
    max-width: 1280px;
    position: relative;
    & > * {
      width: 100%;
    }
    header,
    footer {
      height: var(--ui-navbar-height);
    }
    header {
      left: 0;
      position: absolute;
      top: 0;
      z-index: 10;
    }
  }
</style>
