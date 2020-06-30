<template>
  <div>
    <Nav></Nav>
    <div class="jumbotron">

    </div>
    <Nuxt />
  </div>
</template>

<script>
import Nav from '../components/Nav';
export default {
  components: {
    Nav
  },
   mounted () {
    this.$nextTick(() => {
      this.$nuxt.$loading.start()

      setTimeout(() => this.$nuxt.$loading.finish(), 500)
    })
  }
}
</script>

<style>

</style>
