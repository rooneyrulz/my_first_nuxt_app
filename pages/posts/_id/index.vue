<template>
  <div class="Post">
    <ul class="list-group my-3">
      <li class="list-group-item">
        <strong>Title</strong>
        <br><br>
        <span class="">
          {{ post.title }}
        </span>
      </li>
      <li class="list-group-item">
        <strong>Body</strong>
        <br><br>
        <span class="">
          {{ post.body }}
        </span>
      </li>
      <nuxt-link to="/posts" class="btn btn-back btn-dark">Back</nuxt-link>
    </ul>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  name: 'Post',
  data() {
    return {
      post: {}
    };
  },
  async created() {
    try {
      const { data } = await axios.get(
        `https://jsonplaceholder.typicode.com/posts/${this.$route.params.id}`
      );
      this.post = data;
    } catch (error) {
      console.log(error);
    }
  }
}
</script>

<style scoped>

</style>
