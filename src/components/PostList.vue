<template>
  <div>
      <button @click="getPost">Load post</button>
      <h1 v-if="errorMsg"> {{ errorMsg }}</h1>
      <div v-for="post in posts" :key='post.id'>
      <h3>{{ post.id }}</h3>
      <h2>{{ post.title }}</h2>
      <p>{{ post.body }}</p>
      <hr />
      </div>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  name: 'PostList',
  // mounted(){
  //   this.getPost()
  // },
  data(){
    return{
      posts:[],
      errorMsg:''
    }
  },
  methods:{
    getPost(){
      axios.get('https://jsonplaceholder.typicode.com/posts')
      .then((response)=>{
        console.log(response.data)
        this.posts=response.data
      })
      .catch((error)=>{
        console.log(error)
        this.errorMsg=error
      })
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
