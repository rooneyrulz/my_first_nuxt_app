<template>
  <div class="Post">
    <ul class="list-group my-3">
      <li class="list-group-item">
        <strong>{{ post.title }}</strong>
      </li>
      <li class="list-group-item">
        <span class="">
          <nuxt-link :to="'posts/' + post.id" class="btn btn-view btn-primary">
            View
          </nuxt-link>
          <button @click="$emit('del-post', post.id)" class="btn btn-del btn-danger">
            DELETE
          </button>
        </span>
      </li>
    </ul>
  </div>
</template>

<script>

export default {
  name: 'Post',
  props: {
    post: Object
  }
}
</script>

<style>

</style>
