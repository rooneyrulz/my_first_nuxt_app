<template>
  <div>
    <AppHeader />
    <main class="container">
      <nuxt/>
    </main>
  </div>
</template>

<script>
import AppHeader from "@/components/AppHeader/AppHeader";

export default {
  components: {
    AppHeader
  }
};
</script>


<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-size: 1rem;
  font-weight: 400;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  line-height: 1.5;
  overflow-x: hidden;
}
</style>
