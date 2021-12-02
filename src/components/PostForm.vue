<template>
  <form @submit.prevent="createPost">
    <h4>Создание поста</h4>
    <input
      v-model="post.title"
      class="input"
      type="text"
      placeholder="Название поста"
    >
    <input
      v-model="post.body"
      class="input"
      type="text"
      placeholder="Описание"
    >
    <my-button
      class="btn"
    >
      Создать
    </my-button>
  </form>
</template>

<script>
import MyButton from '@/components/UI/MyButton.vue';

export default {
  name: 'PostForm',
  components: {
    MyButton,
  },
  data() {
    return {
      post: {
        title: '',
        body: '',
      },
    };
  },
  methods: {
    createPost() {
      this.post.id = Date.now();
      this.$emit('create', this.post);
      this.post = {
        title: '',
        body: '',
      };
    },
  },
};
</script>

<style scoped>
form {
  display: flex;
  flex-direction: column;
}
.input {
  border: 1px solid teal;
  padding: 10px 15px;
  margin-top: 10px;
}
</style>
