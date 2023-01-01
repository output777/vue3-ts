<template>
  <div>
    <h2>인기 부트 캠프</h2>
    <ul class="lists">
      <li v-for="camp in camps" :key="camp.id">
        <img src="@/assets/img/image-1.png" alt="campImg" />
        <div class="listInfo">
          <p>
            {{ camp.status === "start" ? "모집중" : "모집" }}
          </p>
          <p class="title">{{ camp.title }}</p>
          <p>{{ camp.startDate }}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script lang="ts">
import Vue from "vue";

interface ICamp {
  id: number;
  status: "before" | "start" | "end";
  title: string;
  startDate: string;
  skill: string;
  img: string;
}

export default Vue.extend({
  name: "AppCamp",
  data: function () {
    const camps: ICamp[] = [
      {
        id: 1,
        status: "start",
        title: "React 실무 프로젝트로 역량 업그레이드",
        startDate: "1월 19일 시작",
        skill: "IT/프론트",
        img: "@/assets/img/image-2.png",
      },
      {
        id: 2,
        status: "start",
        title: "React 실무 프로젝트로 역량 업그레이드",
        startDate: "1월 19일 시작",
        skill: "IT/프론트",
        img: "@/assets/img/image-2.png",
      },
      {
        id: 3,
        status: "start",
        title: "React 실무 프로젝트로 역량 업그레이드",
        startDate: "1월 19일 시작",
        skill: "IT/프론트",
        img: "@/assets/img/image-2.png",
      },
      {
        id: 4,
        status: "start",
        title: "React 실무 프로젝트로 역량 업그레이드",
        startDate: "1월 19일 시작",
        skill: "IT/프론트",
        img: "@/assets/img/image-2.png",
      },
    ];
    return {
      camps,
    };
  },
});
</script>

<style scoped>
.lists {
  display: flex;
  justify-content: space-between;
  margin: 0;
  padding: 0;
}

.lists li {
  height: 280px;
  width: 224px;
  border-radius: 10px;
  position: relative;
}

.lists li img {
  width: 100%;
  height: 100%;
  position: absolute;
  z-index: 1;
}

.lists .listInfo {
  z-index: 10;
  width: 100%;
  position: absolute;
  bottom: 0;
  padding: 16px;
  box-sizing: border-box;
}

.lists .listInfo p {
  color: #eee;
  font-size: 18px;
  padding: 3px 0;
  margin: 0;
  font-family: Noto Sans;
  font-size: 16px;
  font-weight: 500;
  line-height: 18px;
  letter-spacing: -0.01em;
  text-align: left;
}

.lists .listInfo .title {
  color: #fff;
  font-weight: 700;
}
</style>
