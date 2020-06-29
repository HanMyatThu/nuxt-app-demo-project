<template>
  <div>
    <h1>This is user'id {{ $route.params.id }}</h1>
  </div>
</template>

<script>
export default {
  validate(context) {
    return /^\d+$/.test(context.params.id);
  }
}
</script>
