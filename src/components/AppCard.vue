<template>
  <div>
    <h2>커뮤니티</h2>
    <ul class="lists">
      <li v-for="card in cards" :key="card.id">
        <div class="top">
          <p class="views">{{ card.views >= 100 ? "조회수 TOP" : "" }}</p>
          <p class="category">{{ card.category }}</p>
        </div>
        <h3 class="title">{{ card.title }}</h3>
        <p class="descrition">{{ card.descrition }}</p>
        <div class="mentor" v-for="mentor in card.mentors" :key="mentor.id">
          <div class="imgBox">
            <img src="@/assets/img/profile.png" alt="profile" />
          </div>
          <div class="comment">
            <h5>{{ mentor.name }}</h5>
            <p>{{ mentor.comment }}</p>
          </div>
        </div>
        <div class="more">
          <a href="#">+더보기</a>
        </div>
      </li>
    </ul>
  </div>
</template>

<script lang="ts">
import Vue from "vue";

interface ICard {
  id: number;
  views: number;
  category: string;
  title: string;
  descrition: string;
  mentors: IMentors[];
}

interface IMentors {
  id: number;
  img: string;
  name: string;
  comment: string;
}

export default Vue.extend({
  name: "AppCard",
  components: {},
  data: function () {
    const cards: ICard[] = [
      {
        id: 10,
        views: 100,
        category: "취업 고민",
        title: "합격 메일 답장 어떻게 할까요?",
        descrition: "고칠 부분이 있는지 봐주시면 갑사하겠습니다!",
        mentors: [
          {
            id: 100,
            img: "@/assets/img/profile.png",
            name: "멘토1342",
            comment: "안녕하세요. 먼저 면접까지...",
          },
          {
            id: 101,
            img: "@/assets/img/profile.png",
            name: "멘토1342",
            comment: "안녕하세요. 먼저 면접까지...",
          },
        ],
      },
      {
        id: 11,
        views: 100,
        category: "취업 고민",
        title: "합격 메일 답장 어떻게 할까요?",
        descrition: "고칠 부분이 있는지 봐주시면 갑사하겠습니다!",
        mentors: [
          {
            id: 102,
            img: "@/assets/img/profile.png",
            name: "멘토1342",
            comment: "안녕하세요. 먼저 면접까지...",
          },
          {
            id: 103,
            img: "@/assets/img/profile.png",
            name: "멘토1342",
            comment: "안녕하세요. 먼저 면접까지...",
          },
        ],
      },
      {
        id: 12,
        views: 100,
        category: "취업 고민",
        title: "합격 메일 답장 어떻게 할까요?",
        descrition: "고칠 부분이 있는지 봐주시면 갑사하겠습니다!",
        mentors: [
          {
            id: 104,
            img: "@/assets/img/profile.png",
            name: "멘토1342",
            comment: "안녕하세요. 먼저 면접까지...",
          },
          {
            id: 105,
            img: "@/assets/img/profile.png",
            name: "멘토1342",
            comment: "안녕하세요. 먼저 면접까지...",
          },
        ],
      },
      {
        id: 13,
        views: 100,
        category: "취업 고민",
        title: "합격 메일 답장 어떻게 할까요?",
        descrition: "고칠 부분이 있는지 봐주시면 갑사하겠습니다!",
        mentors: [
          {
            id: 106,
            img: "@/assets/img/profile.png",
            name: "멘토1342",
            comment: "안녕하세요. 먼저 면접까지...",
          },
          {
            id: 107,
            img: "@/assets/img/profile.png",
            name: "멘토1342",
            comment: "안녕하세요. 먼저 면접까지...",
          },
        ],
      },
    ];
    return {
      cards,
    };
  },
});
</script>

<style scoped>
.lists {
  display: flex;
  justify-content: space-between;
  padding: 0;
  margin: 0;
  list-style: none;
}

.lists li {
  width: 224px;
  /* height: 320px; */
  border-radius: 10px;
  border: 1px solid #cccccc;
  padding: 16px;
  box-sizing: border-box;
  position: relative;
  box-shadow: 12px 14px 7px -8px rgba(194, 194, 194, 0.78);
  -webkit-box-shadow: 12px 14px 7px -8px rgba(194, 194, 194, 0.78);
  -moz-box-shadow: 12px 14px 7px -8px rgba(194, 194, 194, 0.78);
}

.lists li.title {
  height: 36px;
  width: 191px;
  padding: 0;
  margin: 0;
  font-family: Noto Sans;
  font-size: 16px;
  font-weight: 700;
  line-height: 18px;
  letter-spacing: -0.01em;
  text-align: left;
}

.lists li.descrition {
  height: 36px;
  width: 192px;
  padding: 10px 0 20px 0;
  margin: 0;
  font-family: Noto Sans CJK KR;
  font-size: 14px;
  font-weight: 400;
  line-height: 18px;
  letter-spacing: -0.01em;
  text-align: left;
}

.top {
  display: flex;
  align-items: center;
}

.top p {
  height: 22px;
  width: 67px;
  border-radius: 4px;
  font-family: Noto Sans;
  font-size: 12px;
  font-weight: 700;
  line-height: 14px;
  letter-spacing: -0.01em;
  /* text-align: left; */
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 4px;
}

.top .views {
  background: rgb(89, 215, 154);
  color: #fff;
  margin-right: 10px;
}

.top .category {
  background: #ccc;
  color: #000;
}

.mentor {
  display: flex;
  align-items: center;
  padding: 8px 0;
}

.mentor .imgBox {
  height: 30px;
  width: 30px;
  padding-right: 8px;
}

.mentor .imgBox img {
  width: 100%;
}

.mentor .comment h5 {
  padding: 5px;
  margin: 0;
  height: 16px;
  width: 58px;
  font-family: Noto Sans;
  font-size: 12px;
  font-weight: 700;
  line-height: 14px;
  letter-spacing: -0.01em;
  text-align: left;
}

.mentor .comment p {
  padding: 0;
  margin: 0;
  height: 14px;
  font-family: Roboto;
  font-size: 12px;
  font-weight: 400;
  line-height: 14px;
  letter-spacing: 0em;
  text-align: left;
}

.more {
  display: flex;
  justify-content: center;
  align-items: center;
}
.more a {
  text-decoration: none;
  font-family: Roboto;
  font-size: 12px;
  font-weight: 400;
  line-height: 14px;
  letter-spacing: 0em;
  text-align: left;
  color: #24dbaf;
  padding: 10px;
  display: inline-block;
}
</style>
