<template>
  <div class="container">
    <h1>{{ post.title }}</h1>
    <pre>{{ post.id }}</pre>
    <nuxt-link to="/post"></nuxt-link>
  </div>
</template>

<script>
import axios from 'axios';
export default {
  data() {
    return {
      post: '',
      errors: ''
    }
  },
  async asyncData(context) {
    try {
      let { data } = await axios.get(`https://jsonplaceholder.typicode.com/todos/${context.params.id}`)
      return { post: data};
    } catch(e) {
      return { errors: e};
    }
  },
  head: {
    title : 'A single post'
  }
}
</script>
