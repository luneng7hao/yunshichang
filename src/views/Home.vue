<template>
  <div class="container">
    <div class="main-img" style="height:550px;">
      <!-- <mcloud-carousel></mcloud-carousel> -->
    </div>
    <div class="test">
      <div class="content">
        <div class="item" v-for="item in adv.test" :key="item.id">
          <img :src="item.img" />
          <div class="text">
            <p class="title">{{ item.title }}</p>
            <p>{{ item.title2 }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",
  components: {},
  data() {
    return {
      adv: {
        test: [
          {
            id: "1",
            img: require("@/assets/img/icon_com.png"),
            title: "高质量",
            title2: "123"
          },
          {
            id: "1",
            img: require("@/assets/img/icon_we.png"),
            title: "高质量",
            title2: "123"
          },
          {
            id: "1",
            img: require("@/assets/img/icon_cloud.png"),
            title: "高质量",
            title2: "123"
          }
        ]
      }
    };
  }
};
</script>
<style lang="scss" scoped>
.container {
  .main-img {
    width: 100%;
    text-align: center;
    color: #fff;
  }
}
</style>
