<template>
  <nav>
    <a href="/">Home</a>
    <a href="/blog">Blog</a>
    <a href="/about">About</a>
  </nav>
</template>

<script>
  export default {
    name: 'Navigation',
    data() {
      return {
        msg: 'Ben built this page!'
      }
    }
  }

</script>

<style scoped>
  nav {
    margin: 0 auto;
    position: fixed;
    width: calc(100% - 40px);
    max-width: 960px;
    top: 0;
    left: 50%;
    transform: translate(-50%, 0);
    background: #fff;
    display: flex;
    border-bottom: solid #ddd 1px;
  }

  nav a {
    padding: 10px;
    transition: .3s;
    text-decoration: none;
    color: #555
  }

  nav a:hover {
    background: #444;
    color: #fff;
  }

</style>
