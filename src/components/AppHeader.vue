<template>
  <header>
    <p class="title">mentor</p>
    <div class="user">
      <img src="@/assets/img/user.png" alt="user" />
    </div>
  </header>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  name: "AppHeader",
});
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 16px;
}

.title {
  height: 32px;
  width: 100px;
  color: #fff;

  font-family: Roboto Slab;
  font-size: 24px;
  font-weight: 700;
  line-height: 32px;
  letter-spacing: -0.07em;
  text-align: left;
}

.user img {
  width: 18px;
}
</style>
