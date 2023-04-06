<template>
  <div class="content">
    <div>Likes count {{ likes }}</div>
    <button @click="addLikes">like</button>
    <button @click="addDisLikes">dislike</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      likes: 0
    }
  },
  methods: {
    addLikes(){
      this.likes += 1
    },
    addDisLikes(){
      this.likes -= 1
    }
  }
}
</script>

<style scoped>
.content{
  display: flex;
  flex-direction: column;

}
</style>
