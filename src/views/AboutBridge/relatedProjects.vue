<!--
 * @Author: yanbao dong
 * @Date: 2023-03-27 19:47:38
 * @LastEditors: yanbao dong
 * @LastEditTime: 2023-03-29 18:47:57
 * @Description: file content
-->
<template>
  <div class="relatedProjects">
    <header class="header-box">
      <p class="title-page">{{ topic }}</p>
    </header>
    <main class="main-box">
         <p class="img-list img-list-1" >
        <img src="@/assets/relatedProjects/pro-00.png" alt="" class="pro-img" />
      </p>
      <p class="img-list" v-for="(item, index) in imglist" :key="index">
        <img :src="item.imgSrc" alt="" class="pro-img" />
      </p>
    </main>
  </div>
</template>

<script setup>
import { ref } from "vue";
let topic = ref("RELATED PROJECTS");
// import pro0 from "@/assets/relatedProjects/pro-00.png";
import pro1 from "@/assets/relatedProjects/pro-01.jpeg";
import pro2 from "@/assets/relatedProjects/pro-02.jpeg";
import pro3 from "@/assets/relatedProjects/pro-03.jpeg";
import pro4 from "@/assets/relatedProjects/pro-04.jpeg";
const imglist = ref([

  {
    imgSrc: pro1,
  },
  {
    imgSrc: pro2,
  },
  {
    imgSrc: pro3,
  },
  {
    imgSrc: pro4,
  },
]);
</script>

<style lang="scss">
.relatedProjects {
  min-width: 1200px;
  text-align: left;
  .header-box {
    height: 144px;
    width: 100%;
    background: url(@/assets/page-bc.jpg) no-repeat top center;
    background-size: cover;
    .title-page {
      width: 1200px;
      margin: 0 auto;
      height: 100%;
      padding-top: 48px;
      font-size: 40px;
      line-height: 1.5;
      color: #fff;
      font-weight: 600;
    }
  }
  .main-box {
    width: 1200px;
    margin: 0 auto;
    padding: 90px 30px;
    .img-list {
      width: 100%;
      margin-bottom: -77px;
      .pro-img {
        width: 100%;
      }
      &.img-list-1{
          margin-bottom: -60px;
      }
       &:nth-child(2){
         margin-bottom: 0px;
         position: relative;
        //  z-index: 777;
      }
      &:nth-child(3){
        margin-top: -110px;
         margin-bottom: -140px;
      }
      &:nth-child(4){
         margin-bottom: -122px;
      }
    }
  }
}
</style>
