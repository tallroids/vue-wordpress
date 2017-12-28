<template>
  <div>
    <h1>Recent Posts</h1>
    <div v-for="post in posts">
      <a :href="post.link" class="link">
        <h4>{{post.title.rendered}} | {{post.date}}</h4>
        <p v-html="post.excerpt.rendered"></p>
      </a>
    </div>
  </div>
</template>

<script>
  import Vue from 'vue'
  let posts = [];
  // GET /someUrl

  export default {
    name: 'blog',
    props: ['onLoad'],
    data() {
      return {
        msg: 'Ben built this page!',
        posts: posts
      }
    },
    created: function() {
      this.$http.get('http://harkermedia.com/wp-json/wp/v2/posts?context=embed&per_page=10').then(response => {
        // get body data
        this.posts = response.body;

      }, response => {
        console.err("request failed")
      });
    }
  }

</script>

<style scoped>
  .link {
    text-decoration: none;
    color: #444;
    display: block;
    transition: .3s;
    padding: 10px;
  }
  
  .link:hover{
    background: #eee;
  }
</style>
