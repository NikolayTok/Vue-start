<template lang="">
    <div class="posts" v-for="post in posts">
        <div class="post">
          <p>{{ post.title }}</p>
          <p>{{ post.body }}</p>
        </div>
      </div>
</template>
<script>
export default {
    name: 'posts-list',
    props: {
        posts: {
            type: Array
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
</style>