<template>
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <a class="navbar-brand" href="#">Nuxt App</a>
    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
      <div class="navbar-nav">
        <li class="nav-item">
          <nuxt-link class="nav-link" to='/'>Home</nuxt-link>
        </li>
        <li class="nav-item">
          <nuxt-link class="nav-link" to='/users'>Users</nuxt-link>
        </li>
        <li class="nav-item">
          <nuxt-link class="nav-link" to='/posts'>Posts</nuxt-link>
        </li>
      </div>
    </div>
  </nav>
</template>

<script>
export default {

}
</script>
