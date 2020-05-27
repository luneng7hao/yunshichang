<template>
  <div class="container">
    <div class="main-img">
      <el-carousel indicator-position="inside">
        <el-carousel-item v-for="item in banners" :key="item.id">
          <img :src="item.img" />
        </el-carousel-item>
      </el-carousel>
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
      banners: [
        { id: "1", img: require("@/assets/img/banner1.jpg") },
        { id: "2", img: require("@/assets/img/banner2.jpg") },
        { id: "3", img: require("@/assets/img/banner3.jpg") }
      ],
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
$color-f: #fff;
$color-c: #ccc;
$color-6: #666;
$color-3: #333;
$color-2c: #2c78f4;
.container {
  .main-img {
    width: 100%;
    text-align: center;
    color: #fff;
    letter-spacing: 2px;
    img {
      width: 100%;
      height: 100%;
    }
    .el-carousel__item h3 {
      font-size: 14px;
      opacity: 0.75;
      // line-height: 150px;
      margin: 0;
    }
    ::v-deep.el-carousel__container {
      height: 450px;
    }

    .el-carousel__item:nth-child(2n) {
      background-color: #99a9bf;
    }

    .el-carousel__item:nth-child(2n + 1) {
      background-color: #d3dce6;
    }
  }
  .test {
    position: relative;
    z-index: 99;
    background: rgba(21, 25, 86, 0.65);
    height: 80px;
    transform: translateY(-80px);
    .content {
      height: 100%;
      display: flex;
      justify-content: space-around;
      align-items: center;
      max-width: 1200px;
      margin: 0 auto;
      .item {
        width: 25%;
        display: flex;
        justify-content: center;
        img {
          width: 62px;
          height: 58px;
        }
        .text {
          padding-left: 20px;
          line-height: 120px;

          .title {
            font-family: sans-serif;
            font-size: 16px;
            color: #2c78f4;
            line-height: 24px;
          }
        }
      }
    }
  }
}
</style>
