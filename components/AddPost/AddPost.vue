<template>
  <div class="AddPost mb-5">
    <h1 class="display-4">Add Post</h1>
    <form>
      <div class="form-group">
        <label for="title">Title</label>
        <input id="title" type="text" class="form-control" placeholder="Post Title">
      </div>
      <div class="form-group">
        <label for="body">Body</label>
        <textarea id="body" class="form-control" placeholder="Post Body"></textarea>
      </div>
      <button class="btn btn-add btn-success">
        ADD POST
      </button>
    </form>
  </div>
</template>

<script>
export default {
  name: 'AddPost'
}
</script>

<style>

</style>
