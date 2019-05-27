<template>
  <div class="SearchPost">
      <input @keyup="$emit('search-text', searchText)" v-model="searchText" id="searchText" type="text" class="form-control" placeholder="Search posts">
  </div>
</template>

<script>
export default {
  name: "SearchPost",
  data() {
    return {
      searchText: ""
    };
  }
};
</script>

<style scoped>
</style>
