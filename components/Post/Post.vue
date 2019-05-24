<template>
  <div class="Post">
    <ul class="list-group my-3">
      <li class="list-group-item">
        <strong>{{ post.title }}</strong>
        <span class="float-right">
          <nuxt-link :to="'posts/'+post.id" class="btn btn-view btn-primary">
            View
          </nuxt-link>
          <button class="btn btn-del btn-danger">
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
