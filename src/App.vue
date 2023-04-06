<template>
  <form class="form" @submit.prevent>
    <input v-model="title" class="input" placeholder="Add title" type="text">
    <input v-model="body" class="input" placeholder="Add description" type="text">
    <button @click="createPost" class="btn">Add post</button>
  </form>

  <div class="posts" v-for="post in posts">
    <div class="post">
      <p>{{ post.title }}</p>
      <p>{{ post.description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      posts: [
        { id: 1, title: 'post title 1', description: 'post description 1' },
        { id: 2, title: 'post title 2', description: 'post description 2' },
        { id: 3, title: 'post title 3', description: 'post description 3' }
      ],
      title: '',
      body: '',
    }
  },
  methods: {
    createPost(){
      const newPost = {
        id: Date.now(),
        title: this.title,
        description: this.body,
      }
      this.posts.push(newPost)
      this.title = ''
      this.body = ''
    }
  }
}
</script>

<style scoped>
.post {
  padding: 2rem;
  border: 2px solid green;
  margin-bottom: 1rem;
  border-radius: 20px;
}
.form{
  margin-bottom: 1rem;
  display: flex;
  gap: 1rem; 
}

.input{
  padding: .5rem;
  border-color: #4dbd4d;
  border-radius: 5px;
}

.btn{
  background-color: transparent;
  border-color: #4dbd4d;
}
</style>
