<template>
  <div class="over-view">
    <section class="video-box">
      <iframe id="iframeDom" width="100%" height="100%" src="https://cityuhk-lms.ap.panopto.com/Panopto/Pages/Viewer.aspx?id=fb884123-d0f8-41cf-a05e-b00b00318d6f" title="YouTube video player" frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture;"
        allowfullscreen></iframe>
      <!-- <video class="video-play"  controls muted autoplay loop>
        <source src="" type="video/mp4">
        <p> 当前浏览器不支持video标签 </p>
      </video> -->
      <!-- src="https://www.youtube.com/embed/wrbEwN49rQ8"  -->
    </section>
    <header class="header header-22">
      <el-carousel indicator-position="outside" autoplay :pause-on-hover="false" :interval='4000'>
        <el-carousel-item v-for="(item, index) in imgList" :key="index">
          <img :src="item.imgSrc" alt="" class="pic-class" />
        </el-carousel-item>
      </el-carousel>
    </header>
    <!-- 文字内容区域 -->
    <main class="mian">
      <section class="section-left">
        <p class="title">Pathways to Impact</p>
        <Article></Article>
      </section>
      <section class="section-right">
        <p class="title">
          <span class="left-label">Past Events</span>
          <span class="right-label">See all upcoming events</span>
        </p>
        <div class="work-shop">
          <div class="left-date">
            <span class="number-data">9</span>
            <span class="month-data">March</span>
          </div>
          <div class="right">
            <p class="title-top">
              Workshop on Social Determinant of Health
            </p>
            <p class="desc-1">
              <span class="label"> Speaker(s): </span>
              <span class="value">
                Dr. Nicole Valentine, Dr. Stephen Jan, Mr. Michael Jacobson, Dr. Carmel Williams
              </span>
            </p>
            <p class="desc-2">
              <span class="label">Time: </span>
              <span class="value">March 9 2023， 2:00pm-4:45pm</span>
            </p>
            <p class="desc-2">
              <span class="label">Venue: </span>
              <span class="value">G7603, Yeung Kin Man Academic Building (YEUNG)</span>
            </p>
            <p class="desc-4" @click="learnAndBook">Read More</p>
          </div>
        </div>
      </section>
       <!-- <p class="title-2">Past Webinars</p>
        <Webinars></Webinars> -->
    </main>

    <div class="line-wrap"></div>
    <!-- partners -->
    <Parteners></Parteners>
  </div>
</template>

<script setup>
import { useRouter } from "vue-router";
const router = useRouter();
import Article from "@/components/Article.vue";
import Parteners from "@/components/Parteners.vue";
import { ElCarousel, ElCarouselItem } from "element-plus";
import "element-plus/es/components/carousel/style/css";
import "element-plus/es/components/carousel-item/style/css";
import {ref } from "vue";
import pic01 from "@/assets/banners-001.jpeg";
import pic02 from "@/assets/banners-002.jpeg";
import pic03 from "@/assets/banners-003.jpeg";
let imgList = ref([
  {
    imgSrc: pic01,
  },
  {
    imgSrc: pic02,
  },
  {
    imgSrc: pic03,
  },
]);
const learnAndBook = () => {
  //webinars
  router.push({
      path: "/webinars",
    });
};



</script>

<style lang="scss">
.el-carousel {}

.el-carousel__container {
  width: 1400px;
  margin: 0 auto;
  height: 652px;
}

.el-carousel__item {
  .pic-class {

    height: 652px;
  }
}

.over-view {
  min-width: 1200px;
  text-align: left;

  .header {
    width: 100%;
    height: 682px;
    background-color: #fff;
    text-align: center;

    &.header-22 {
      border-bottom: none;
    }
  }

  .mian {
    width: 1200px;
    margin: 0 auto;
    padding: 35px 0px;

    .section-left {
      flex: 1.5;

      // border-right: 1px solid #ddd;
      .title {
        font-size: 30px;
        line-height: 1.5;
        color: #4a4a4a;
        font-weight: 600;
        margin-bottom: 25px;
      }
    }

    .section-right {
      margin-top: 60px;

      .title {
        display: flex;
        justify-content: space-between;
        margin-bottom: 25px;
        align-items: center;

        .left-label {
          font-size: 30px;
          line-height: 1.5;
          color: #4a4a4a;
          font-weight: 600;
        }

        .right-label {
          cursor: pointer;
        }
      }

      .work-shop {
        height: 290px;
        position: relative;
        background: rgb(167, 219, 251);
        overflow: hidden;

        .left-date {
          width: 180px;
          height: 180px;
          border-radius: 50%;
          background: #49b4f7;
          position: absolute;
          left: -30px;
          top: -40px;

          .number-data {
            position: absolute;
            top: 40px;
            right: 65px;
            font-size: 60px;
            line-height: 1.5;
            color: #fff;
            font-weight: 700;
          }

          .month-data {
            position: absolute;
            font-size: 30px;
            line-height: 1.5;
            color: #fff;
            font-weight: 700;
            top: 110px;
            right: 35px;
          }
        }

        .right {
          margin-left: 200px;
          margin-top: 20px;
          margin-right: 60px;

          .title-top {
            font-size: 20px;
            line-height: 1.5;
            color: #222;
            font-weight: 600;
          }

          .desc-1 {
            font-size: 16px;
            line-height: 1.5;
            color: #222;
            margin: 20px 0;

            .label {
              font-weight: 600;
              margin-right: 10px;
            }
          }

          .desc-2 {
            font-size: 16px;
            line-height: 1.5;
            color: #222;
            margin: 20px 0;

            .label {
              font-weight: 600;
              margin-right: 10px;
            }
          }

          .desc-4 {
            display: inline-block;
            font-size: 14px;
            line-height: 1.5;
            padding: 8px 30px;
            border-radius: 20px;
            color: #222;
            font-weight: 600;
            background: rgb(67, 160, 234);
            cursor: pointer;
          }
        }
      }

      .title-2 {
        padding: 17px;
        font-size: 15px;
        font-weight: 600;
        color: #c72b39;
      }
    }
  }

  .video-box {
    width: 1200px;
    margin: 0 auto;
    padding: 0px 0px 50px;
    height: 745px;
    .video-play{
      width: 100%;
      height: 100%;
    }
  }

  .line-wrap {
    width: 950px;
    height: 1px;
    color: rgba(176, 176, 176, 0.5);
    background-color: rgba(176, 176, 176, 0.5);
    margin: 20px auto;
  }
}
</style>
