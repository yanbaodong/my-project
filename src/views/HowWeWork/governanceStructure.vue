<template>
    <div class="governance-structure">
      <header class="header-box">
        <p class="title-page">{{ topic }}</p>
      </header>
      <main class="main-box">
        <img class="img-01" src="@/assets/governanceStructure/governance-structure.jpeg" alt="">
      </main>
    </div>
  </template>
  
  <script setup>
  import { ref } from "vue";
  let topic = ref("GOVERANCE STRUCTURE");
  </script>
  
  <style lang="scss">
  .governance-structure {
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
      .img-01{
        width: 100%;
      }
    }
  }
  </style>
  