<template>
  <div id="main">
    <blog></blog>
  </div>
</template>

<script>
  import blog from './Blog'
  export default {
    name: 'Home',
    components: {
      blog
    },
    data() {
      return {
        msg: 'Ben built this page!'
      }
    }
  }

</script>

<style scoped>
  #main {
    background: #fff;
    overflow: hidden;
    padding: 5px 20px;
    max-width: 960px;
    margin-top: 40px;
    margin: 40px auto 20px;
  }

</style>
