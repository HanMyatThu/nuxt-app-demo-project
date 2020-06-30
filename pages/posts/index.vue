<template>
  <div class="container">
    <h2>Api Request Vue Way</h2>
    <div class="row">
      <Card v-for="post in posts" :key="post.id" :post="post" class="col-md-4"></Card>
      <button class="btn btn-danger" v-scroll-to="{ el : 'body'}">Back to Top</button>
    </div>
    <!-- <div v-for="post in posts" :key="post.id" class="card">
      <div class="card-body">
        <h2>{{ post.title }}</h2>
      </div>
    </div> -->
  </div>
</template>

<script>
import axios from 'axios';
import Card from '@/components/Card'
import { mapGetters } from 'vuex';

export default {
  components : {
    Card
  },
  data() {
    return {
      allPosts: [],
      errors: ''
    }
  },
  computed: {
    ...mapGetters( ['posts'])
    // allPosts() {
    //   return this.$store.getters.posts;
    // }
  },
  // async fetch({ store }) {
  //   try {
  //     let { data } = await axios.get('https://jsonplaceholder.typicode.com/todos');
  //     store.dispatch('setPosts',data);
  //     // return { allPosts: data};
  //   } catch(e) {
  //     return { errors: e};
  //   }
  // },
  head: {
    title : 'List of Posts'
  }
}
</script>
