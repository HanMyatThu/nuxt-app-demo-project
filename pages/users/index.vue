<template>
  <div class="container">
    <h1>Hello users</h1>

    <input type="text" v-model='id'>
    <button @click='loadUser'>Load User</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      id: null,
    }
  },
  methods: {
    loadUser() {
      this.$router.push(`/users/${this.id}`)
    }
  }
}
</script>

<style>

</style>
