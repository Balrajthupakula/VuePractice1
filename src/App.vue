<template>
  <div class="app">
    <CreatePost />
    <PostList />
    <LifeCycle /><br>
    <ClickCounter /><br>

    <HoverCounter />
  </div>
</template>

<script>
import PostList from './components/PostList.vue'
import CreatePost from './components/CreatePost.vue'
import LifeCycle from './components/LifeCycle.vue'
import ClickCounter from './components/ClickCounter.vue'
import HoverCounter from './components/HoverCounter.vue'

export default {
  name: 'App',
  components: {
    PostList,
    CreatePost,
    LifeCycle,
    ClickCounter,
    HoverCounter

  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
