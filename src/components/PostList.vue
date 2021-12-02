<template>
  <div class="post" v-for="post in posts" :key="post.id">
    <div><strong>Название:</strong> {{ post.title }}</div>
    <div><strong>Описание:</strong> {{ post.body }}</div>
  </div>
</template>

<script>
export default {
  name: 'PostList',
  props: {
    posts: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style scoped>
.post {
  margin-top: 16px;
  padding: 15px;
  border: 2px solid teal;
}
</style>
