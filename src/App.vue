<template>
  <div class="app">
    <post-form @create="createPost"/>
    <post-list :posts="posts"/>
  </div>
</template>

<script>
import PostForm from '@/components/PostForm.vue';
import PostList from '@/components/PostList.vue';

export default {
  components: { PostForm, PostList },
  data() {
    return {
      posts: [
        { id: 1, title: 'JS1', body: 'JS description' },
        { id: 2, title: 'JS1', body: 'JS description' },
        { id: 3, title: 'JS1', body: 'JS description' },
      ],
      title: '',
      body: '',
    };
  },
  methods: {
    createPost(post) {
      this.posts.push(post);
    },
  },
};
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.app {
  padding: 10px;
}
</style>
