<template>
  <div id="app">
    <blogHeader />
    <container size="l">
      <storiesBlock rowSize="s">
        <postItem 
          v-for="(post, index) in posts" 
          v-bind:key="post.id" 
          :title="post.title" 
          :subtitle="post.subtitle" 
          :image="post.image" 
          :likes="post.likes" 
          :vertical="(index+1)%4!=0" 
        />
      </storiesBlock>
    </container>
  </div>
</template>

<script>
import data from './data.js'
import blogHeader from './components/blogHeader.vue'
import container from './components/container.vue'
import storiesBlock from './components/storiesBlock.vue'
import postItem from './components/postItem.vue'

export default {
  name: 'App',
  components: {
    blogHeader,
    storiesBlock,
    container,
    postItem
  },
  data() {
    return {posts: data}
  }
}
</script>

<style>
body {
  font-family: 'Ubuntu', Helvetica, Verdana, sans-serif;
  margin: 0;
}
</style>
