<template>
  <div class="app">
    <form>
      <h4>Создание поста</h4>
      <input class="input" type="text" placeholder="Название поста">
      <input class="input" type="text" placeholder="Описание">
      <button class="btn">Создать</button>
    </form>
    <div class="post" v-for="post in posts" :key="post.id">
      <div><strong>{{ post.title }}</strong> {{ post.body }}</div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      posts: [
        { id: 1, title: 'JS1', body: 'JS description' },
        { id: 2, title: 'JS1', body: 'JS description' },
        { id: 3, title: 'JS1', body: 'JS description' },
      ],
    };
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
.post {
  margin-top: 16px;
  padding: 15px;
  border: 2px solid teal;
}
form {
  display: flex;
  flex-direction: column;
}
.input {
  width: 100%;
  border: 1px solid teal;
  padding: 10px 15px;
  margin-top: 10px;
}
.btn {
  margin-top: 15px;
  align-self: flex-end;
  padding: 10px 15px;
  background: none;
  color: teal;
  border: 1px solid teal;
}
</style>
