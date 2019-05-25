<template>
  <header class="mb-5">
    <nav class="navbar navbar-expand-sm navbar-dark bg-dark">
      <div class="container">
        <nuxt-link class="navbar-brand" to="/">Posts Collection</nuxt-link>
        <button
          class="navbar-toggler d-lg-none"
          type="button"
          data-toggle="collapse"
          data-target="#collapsibleNavId"
          aria-controls="collapsibleNavId"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="collapsibleNavId">
          <ul class="navbar-nav mr-auto mt-2 mt-lg-0">
            <li class="nav-item">
              <nuxt-link class="nav-link" to="/">HOME</nuxt-link>
            </li>
            <li class="nav-item">
              <nuxt-link class="nav-link" to="/posts">POSTS</nuxt-link>
            </li>
            <li class="nav-item">
              <nuxt-link class="nav-link" to="/about">ABOUT</nuxt-link>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </header>
</template>

<script>
export default {};
</script>

<style scoped>
.nuxt-link-exact-active {
  color: #f4f4f4 !important;
}
</style>
