<template>
  <div>
    <div class="home-header-container">
      <div class="home">
        <AppHeader></AppHeader>
        <AppHeaderSection></AppHeaderSection>
      </div>
    </div>
    <div class="main">
      <AppCamp></AppCamp>
      <AppCamp></AppCamp>
      <div class="subTitleBox">
        <h2>현직자와 소통하며 배우는 실무 스킬, 퍼스널 트레이닝</h2>
      </div>
      <AppCard></AppCard>
    </div>
    <div class="home-footer-container">
      <div class="footer">
        <AppFooter></AppFooter>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import AppHeader from "@/components/AppHeader.vue";
import AppHeaderSection from "@/components/AppHeaderSection.vue";
import AppCard from "@/components/AppCard.vue";
import AppCamp from "@/components/AppCamp.vue";
import AppFooter from "@/components/AppFooter.vue";

export default Vue.extend({
  name: "AppHome",
  components: {
    AppHeader,
    AppHeaderSection,
    AppCard,
    AppCamp,
    AppFooter,
  },
});
</script>

<style scoped>
.home-header-container {
  width: 100%;
  height: 550px;
  background: rgb(89, 215, 154);
  background: linear-gradient(
    90deg,
    rgba(89, 215, 154, 1) 60%,
    rgba(30, 168, 113, 1) 89%
  );
  overflow: hidden;
}

.home {
  width: 100%;
  max-width: 960px;
  margin: auto;
}

.home h2 {
  padding-top: 50px;
}

.main {
  width: 100%;
  max-width: 960px;
  margin: auto;
}

.subTitleBox {
  height: 100px;
  width: 960px;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 0px;
  margin: 50px 0;
  background: rgb(89, 215, 154);
  background: linear-gradient(
    90deg,
    rgba(89, 215, 154, 1) 60%,
    rgba(30, 168, 113, 1) 89%
  );
}

.subTitleBox h2 {
  padding: 0;
  color: #fff;
}

.home-footer-container {
  width: 100%;
  margin-top: 240px;
  height: 160px;
  background: #eee;
}

.footer {
  width: 100%;
  max-width: 960px;
  margin: auto;
}
</style>
