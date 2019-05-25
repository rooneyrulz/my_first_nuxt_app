<template>
  <div class="Post">
    <Spinner v-if="loading" />
    <div v-if="!loading">
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
  </div>
</template>

<script>
import axios from 'axios';
import Spinner from '@/components/Spinner/Spinner';

export default {
  name: 'Post',
  components: {
    Spinner
  },
  data() {
    return {
      post: {},
      loading: true
    };
  },
  async created() {
    try {
      const { data } = await axios.get(
        `https://jsonplaceholder.typicode.com/posts/${this.$route.params.id}`
      );
      this.post = data;
      this.loading = false;
    } catch (error) {
      console.log(error);
    }
  }
}
</script>

<style scoped>

</style>
