<template>
  <div class="Posts">
    <AddPost/>
    <div>
      <h1 class="display-4">Posts</h1>
      <Post v-for="post in posts" :post="post" :key="post.id"/>
    </div>
  </div>
</template>

<script>
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
      posts: [
        {
          id: "320320",
          title: "Post One",
          body: "This is post one"
        },
        {
          id: "473847",
          title: "Post Two",
          body: "This is post two"
        },
        {
          id: "382383",
          title: "Post Three",
          body: "This is post three"
        }
      ]
    };
  }
};
</script>

<style scoped>
</style>
