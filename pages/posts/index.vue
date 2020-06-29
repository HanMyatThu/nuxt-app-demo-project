<template>
  <div class="container">
    <h2>Api Request Vue Way</h2>
    <div v-for="post in posts" :key="post.id" class="card">
      <div class="card-body">
        <h2>{{ post.title }}</h2>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios';
export default {
  data() {
    return {
      posts: []
    }
  },
  mounted() {
    axios.get('https://jsonplaceholder.typicode.com/todos')
      .then(res => {
        console.log(res.data);
        this.posts = res.data;
      })
      .catch(e => console.log(e))
  }
}
</script>
