<template>
  <div id="app">
    <navigation></navigation>
    <router-view/>
  </div>
</template>

<script>
  import navigation from './components/Navigation'
  export default {
    name: 'app',
    components: {
      navigation: navigation
    }
  }

</script>

<style>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #2c3e50;
    margin: 0 auto;
    background: #eee;
    overflow: hidden;
    padding: 0 20px;
    position: relative;
  }

</style>
