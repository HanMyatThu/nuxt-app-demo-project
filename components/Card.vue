<template>
  <div>
    <div class="card bg-light mb-3">
      <div class="card-header">
        {{ post.id }}
      </div>
      <div class="card-body">
        <p class="card-text">
          <nuxt-link :to='{name: "posts-id", params: {id : post.id }}'>{{ post.title }}</nuxt-link>
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    post : Object
  }
}
</script>
