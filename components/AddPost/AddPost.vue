<template>
  <div class="AddPost mb-5">
    <h1 class="display-4">Add Post</h1>
    <form @submit.prevent="addPost">
      <div class="form-group">
        <label for="title">Title</label>
        <input v-model="title" id="title" type="text" class="form-control" placeholder="Post Title">
      </div>
      <div class="form-group">
        <label for="body">Body</label>
        <textarea v-model="body" id="body" class="form-control" placeholder="Post Body"></textarea>
      </div>
      <button class="btn btn-add btn-success">ADD POST</button>
    </form>
  </div>
</template>

<script>
export default {
  name: "AddPost",
  data() {
    return {
      title: "",
      body: ""
    };
  },
  methods: {
    addPost() {
      if (!this.title || !this.body) {
        alert("Please fill out all fields!");
      }

      this.$emit("add-post", { title: this.title, body: this.body });
    }
  }
};
</script>

<style>
</style>
