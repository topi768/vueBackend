<template>
<TheHeader></TheHeader>



</template>

<script>
import TheHeader from '@/components/TheHeader'
export default {
  components: {
    TheHeader
  },
  data() {
    return {
      posts: [
        {id: 1, title: 'adw', body: 'adwdadawd'},
        {id: 2, title: 'adw2', body: 'adwdadawd'},
        {id: 3, title: 'adw3', body: 'adwdadawd'},

      ]
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.posts__post {
  border: 2px solid green ;
  margin: 5px 0;
}
</style>
