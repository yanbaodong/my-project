<!--
 * @Author: yanbao dong
 * @Date: 2023-01-04 21:30:47
 * @LastEditors: yanbao dong
 * @LastEditTime: 2023-01-10 18:50:13
 * @Description: file content
-->
<template>
  <div class="roadmap">
    <header class="header-box">
      <p class="title-page">{{ topic }}</p>
    </header>
    <main class="main-box">
      <p class="title">
        Hong Kong’s road to pandemic recovery needs to be envisioned with a
        long-term goal of building a
        <span class="to-resilient" @click="toResilient('resilience')">resilient</span>
        society with the capacity to bridge existing and emerging gaps so as to
        absorb future shocks.
      </p>
      <p class="peitu">
        <img src="@/assets/pageImg/page-img-01.png" alt="" class="img-page" />
      </p>
      <p class="text-1 margin0">
        Our ultimate goal is to facilitate Hong Kong’s recovery from the
        COVID-19 pandemic, help it withstand future adverse shocks, and sustain
        economic growth and social equality.
      </p>
      <p class="title-weight">Goals:</p>
      <p class="list-text-1">
        <span class="left-num">[G1]</span>
        <span class="right-text">To develop and theorize a <i class="weight">framework</i>  (Figure 1) for building resilience that connects the
          public, stakeholders, and policymakers.</span>
      </p>
      <p class="list-text-1">
        <span class="left-num">[G2]</span>
        <span class="right-text">To identify and monitor <i class="weight">policy-preference gaps</i>  between the public and
          policymakers.</span>
      </p>
      <p class="list-text-1">
        <span class="left-num">[G3]</span>
        <span class="right-text">To describe the <i class="weight">trustdemic</i> in Hong Kong by identifying gaps between government policies
          and public opinions and analyzing its underlying <i class="weight">mechanisms</i> for different types of trust.</span>
      </p>
      <p class="list-text-1">
        <span class="left-num">[G4]</span>
        <span class="right-text">To understand distrust among peculiar sections of the population, including distrust of
          the <i class="weight">well-off populations</i> in Hong Kong and barriers to information trust for <i class="weight">socially disadvantaged groups</i>.
        </span>
      </p>
      <p class="list-text-1">
        <span class="left-num">[G5]</span>
        <span class="right-text">To build practical guidelines, policy recommendations, and reference tools to increase
          trust.</span>
      </p>
      <p class="list-text-1">
        <span class="left-num">[G6]</span>
        <span class="right-text">To create a <i class="weight">BRIDGE platform</i> that serves as a central hub connecting multiple parties,
          facilitating two-way communication and collaboration within the BRIDGE alliance in the civic sphere.</span>
      </p>




    </main>
  </div>
</template>

<script setup>
import { ref } from "vue";
let topic = ref("Roadmap");

// import { useRoute, useRouter } from "vue-router";
// const router = useRouter();
// const route = useRoute();
// const toResilient = (params) => {
//   const pathMap = {
//     resilience: "/resilience",
//     trust: "/trust",
//     communication: "/communication",
//     informationAndTechnology: "/informationAndTechnology",
//   };
//   router.push({
//     path: pathMap[params],
//   });
// };
</script>

<style lang="scss">
.roadmap {
  min-width: 1200px;
  text-align: left;
  line-height: 1.5;
  font-size: 20px;

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

    .to-resilient {
      text-decoration: underline;
      cursor: pointer;
    }

    .title {
      font-size: 20px;
      font-weight: 600;
    }

    .peitu {
      text-align: center;

      .img-page {
        width: 100%;
      }
    }

    .text-1 {
      margin-top: 30px;

      &.margin0 {
        margin-top: 0;
      }
    }

    .title-weight {
      margin: 30px 0 10px;
      font-weight: 600;
    }

      .weight {
        font-weight: 600;
      }

        .list-text-1 {
          margin-bottom: 15px;
          display: flex;
          .left-num{
            width: 45px;
            font-weight: 600;
          }
          .right-text{
            flex: 1;
          }
          
        }

       
      
    
  }
}</style>
