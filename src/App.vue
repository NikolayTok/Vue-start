<template>
  <post-form @create="createPost"/>
  <post-list :posts="posts"/>
</template>   

<script>

import PostForm from './components/PostForm.vue';
import PostList from './components/PostList.vue';

export default {
  components: {
    PostForm, PostList
  },
  data() {
    return {
      posts: [
        { id: 1, title: 'post title 1', body: 'post description 1' },
        { id: 2, title: 'post title 2', body: 'post description 2' },
        { id: 3, title: 'post title 3', body: 'post description 3' }
      ],
    }
  },
  methods: {
    createPost(post){
      this.posts.push(post)
    }
  }
}
</script>

<style scoped>
.btn{
  background-color: transparent;
  border-color: #4dbd4d;
}
</style>
