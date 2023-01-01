<template>
  <div class="header-section-container">
    <div>
      <p class="desc">
        개발은 <br />
        카페인과 함께
      </p>
      <div class="line-icons">
        <div class="line"></div>
        <div class="iconBox">
          <img src="../assets/img/leftArrow.png" alt="leftArrow" />
          <img src="../assets/img/rightArrow.png" alt="rightArrow" />
        </div>
      </div>
    </div>
    <div class="imgBox">
      <img src="@/assets/img/headerImg.png" alt="headerImg" />
    </div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  name: "AppHeaderSection",
});
</script>

<style scoped>
.header-section-container {
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
}

.desc {
  font-family: Noto Sans;
  font-size: 48px;
  font-weight: 700;
  line-height: 65px;
  letter-spacing: 0em;
  text-align: left;
  color: #fff;
  position: relative;
}

.imgBox {
  height: 400px;
  width: 600px;
  left: 600px;
  top: 104px;
  border-radius: 10px;
}

.imgBox img {
  width: 100%;
}

.line-icons {
  display: flex;
  align-items: center;
}

.line {
  height: 2px;
  width: 245px;
  background-color: #fff;
}

.iconBox img {
  width: 14px;
  padding: 0 10px;
}
</style>
