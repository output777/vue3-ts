<template>
  <div>
    <div class="footer">
      <p class="title">mentor</p>
      <div class="info">
        <p>대표: 내이름. 서울특별시 중구 한강대로 416, 서울스퀘어 15층 101호</p>
        <p>Copyright by (주) mentor. All right reserved.</p>
        <div>
          <span>이용약관</span>
          <span>개인정보처리방침</span>
        </div>
      </div>
      <div class="user">
        <img src="@/assets/img/ellipse.png" alt="ellipse" />
        <img src="@/assets/img/ellipse.png" alt="ellipse" />
        <img src="@/assets/img/ellipse.png" alt="ellipse" />
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  name: "AppFooter",
});
</script>

<style scoped>
.footer {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  padding: 0 16px;
  padding-top: 32px;
}

.title {
  height: 32px;
  width: 100px;
  color: rgb(89, 215, 154);
  margin: 0;
  padding: 0;
  font-family: Roboto Slab;
  font-size: 24px;
  font-weight: 700;
  line-height: 32px;
  letter-spacing: -0.07em;
  text-align: left;
}

.info p {
  margin: 0;
  padding: 0;
  color: #616161;
}
.info p:first-child {
  padding-bottom: 16px;
}

.info span {
  margin: 0;
  padding: 0;
  color: #616161;
}

.user img {
  width: 18px;
  padding: 0 5px;
}
</style>
