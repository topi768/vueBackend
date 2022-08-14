<template>
    <h1 >home</h1>
    <div class="posts" >
        <div 
        class="posts__post"
        v-for="post in posts"
        :key="post.id"
        
        >
        <h2>{{post.id}} {{post.title}}</h2>
        <div>{{post.body}}</div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
export default {
      data() {
        return {
        posts: []
    }
  },
  methods: {
      async fetchPosts() {
        try {
            const response = await axios.get('https://jsonplaceholder.typicode.com/posts', {
                    
            });

            this.posts = response.data
        } catch (e) {

        } finally {

        }
        
      }
  },
  mounted() {
      this.fetchPosts()
  }

}
</script>