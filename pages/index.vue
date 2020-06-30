<template>
  <div class="container">
    <h1>Hello</h1>
    <no-ssr>
      <v-select
        v-model="selected"
        placeholder="Select Category"
        :options="[{label: 'Canada', code: 'ca'}]">

     </v-select>
    </no-ssr>
  </div>
</template>

<script>
export default {
  data() {
    return {
      selected: ''
    }
  }
}
</script>

<style>

</style>
