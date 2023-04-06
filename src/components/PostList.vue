<template lang="">
    <div class="posts" v-for="post in posts">
        <div class="post">
          <p>{{ post.title }}</p>
          <p>{{ post.description }}</p>
        </div>
      </div>
</template>
<script>
export default {
    name: 'posts-list'
}
</script>
<style lang="">
    
</style>