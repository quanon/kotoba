<template lang="pug">
  #app.container
    quotes
</template>

<script>
  import Quotes from './components/Quotes';

  export default {
    name: 'app',
    components: {
      Quotes
    }
  };
</script>

<style lang="scss">
  @import './assets/stylesheets/main.scss';

  #app {
    font-family: "Mplus 1p";
    height: 100%;

    display: flex;
    justify-content: center;
    align-items: center;
  }
</style>
