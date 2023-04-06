<template lang="">
    <form class="form" @submit.prevent>
        <input v-model="post.title" class="input" placeholder="Add title" type="text">
        <input v-model="post.body" class="input" placeholder="Add description" type="text">
        <button @click="createPost" class="btn">Add post</button>
    </form>
</template>
<script>
export default {
    name: 'post-form',
    data() {
        return {
            post: {
                title: '',
                body: ''
            }
        }
    },
    methods: {
        createPost() {
            this.post.id = Date.now()
            this.$emit('create', this.post)
            this.post = {
                title: '',
                body: ''
            }
        }
    }
}
</script>
<style scoped>
.form {
    margin-bottom: 1rem;
    display: flex;
    gap: 1rem;
}

.input {
    padding: .5rem;
    border-color: #4dbd4d;
    border-radius: 5px;
}
</style>