<template>
  <div id="app">
    <AppHome></AppHome>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import AppHome from "./pages/AppHome.vue";

export default Vue.extend({
  name: "App",
  components: {
    AppHome,
  },
});
</script>

<style>
body {
  margin: 0;
}

li {
  list-style: none;
}
</style>
