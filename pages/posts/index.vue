<template>
  <div class="Posts">
    <AddPost v-on:add-post="addPost"/>
    <div>
      <h1 class="display-4">Posts</h1>
      <Post v-for="post in posts" :post="post" :key="post.id" v-on:del-post="deletePost"/>
    </div>
  </div>
</template>

<script>
import axios from "axios";

import Post from "@/components/Post/Post";
import AddPost from "@/components/AddPost/AddPost";

export default {
  name: "Posts",
  components: {
    Post,
    AddPost
  },
  data() {
    return {
      posts: []
    };
  },
  async created() {
    try {
      const { data } = await axios.get(
        "https://jsonplaceholder.typicode.com/posts"
      );
      this.posts = data.slice(0, 10);
    } catch (error) {
      console.log(error);
    }
  },
  methods: {
    async deletePost(id) {
      if (confirm("Are you want to delete this post?")) {
        try {
          const res = await axios.delete(
            `https://jsonplaceholder.typicode.com/posts/${id}`
          );
          this.posts = this.posts.filter(post => {
            return post.id !== id;
          });
        } catch (error) {
          console.log(error);
        }
      }
    },
    async addPost(payload) {
      try {
        const { data } = await axios.post(
          `https://jsonplaceholder.typicode.com/posts`,
          payload
        );
        this.posts = [data, ...this.posts];
      } catch (error) {
        console.log(error);
      }
    }
  }
};
</script>

<style scoped>
  
</style>
