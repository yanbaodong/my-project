<template>
  <div class="deliverables-box">
    <header class="header-box">
      <p class="title-page">{{ topic }}</p>
    </header>

    <main class="main-box">
      <p class="main-text">
        We will construct a <i class="weight"></i> Hong Kong BRIDGE Platform, which includes BRIDGE.org (a web-based platform) and BRIDGE Alliance (an offline consortium), for compiling and disseminating findings and resources.
      </p>
      <section class="list-item" >
        <p class="title-num">[D1]</p>
        <div class="text-box">
          Three <i class="weight">BRIDGE databases: Hong Kong Social Pulse Database</i> (SP1), <i class="weight">Trust and Resilience Survey Database</i> (SP2), and <i class="weight">Digital Health Trend Survey Database</i> (SP4). 
        </div>
     
      </section>
      <section class="list-item" >
        <p class="title-num">[D2]</p>
        <div class="text-box">
          <i class="weight">Annual BRIDGE reports</i> for various stakeholders, including 
          <p class="text-sub-1">
            (a) a Hong Kong Social Pulse Report & Social Signal Model of Pandemic Resilience (SP1), 
          </p>
          <p class="text-sub-1">
            (b) a Trust and Resilience Index Report (SP2), 
          </p>
          <p class="text-sub-1">
            (c) a Technical Report on Hong Kong Expatriate Emigration (SP3), 
          </p>
          <p class="text-sub-1">
            (d) a Hong Kong Digital Health Trend Survey Report (SP4), and
          </p>
          <p class="text-sub-1">
            (e) an Interview Report on Trust & Social Disparity (SP5). 
          </p>
        </div>
     
      </section>
      <section class="list-item" >
        <p class="title-num">[D3]</p>
        <div class="text-box">
          <i class="weight">Hong Kong Resilience & Trust Index</i> based on the findings of SP2, SP3, and SP4, with a variety of economic, health, and information behaviors as indicators (e.g., resilience, app adoption, voting, vaccination, donation, etc.)
        </div>
     
      </section>
      <section class="list-item" >
        <p class="title-num">[D4]</p>
        <div class="text-box">
          <i class="weight">Risk Policy Gap Inventory</i> (SP1) and <i class="weight">Rebuilding Trust Policy Guidelines</i> (SP4-5), which will provide evidence-based guidelines with special attention to disadvantaged groups. 
        </div>
     
      </section>
      <section class="list-item" >
        <p class="title-num">[D5]</p>
        <div class="text-box">
          <i class="weight">Hong Kong Talent Flow Barometer</i> (SP3), which assists policymakers and corporations in tracking the talent flow of different demographics and optimizing the recruitment of global talent.
        </div>
     
      </section>
      <section class="list-item" >
        <p class="title-num">[D6]</p>
        <div class="text-box">
          <i class="weight">Hong Kong e-Health blueprint</i> (SP4), which benchmarks Hong Kong against other regions and guides the development of an Effective and Equal eHealth system (the 3E system).
        </div>
     
      </section>
      <section class="list-item" >
        <p class="title-num">[D1]</p>
        <div class="text-box">
          <i class="weight">Trust-Enhancing Communication Framework: Strategies, Guidelines, and Messages</i> (SP6), which provides a collection of scientifically validated strategies and message templates.
        </div>
      </section>
    </main>
  </div>
</template>

<script setup>
import { ref } from "vue";
let topic = ref("Deliverables");
// const list = ref([
//   {
//     title: "D1. BRIDGE Databases",
//     contentList: [
//       {
//         item: "a. Hong Kong Social Pulse Database ",
//       },
//       {
//         item: "b. Trust and Resilience Survey Database ",
//       },
//       {
//         item: "c. Digital Health Trend Survey Database ",
//       },
//     ],
//   },
//   {
//     title: "D2. Annual BRIDGE Reports",
//     contentList: [
//       {
//         item: "a. Hong Kong Social Pulse Report & Social Signal Model of Pandemic Resilience",
//       },
//       {
//         item: "b. Trust and Resilience Index Report",
//       },
//       {
//         item: "c. Technical Report on Hong Kong Expatriate Emigration & Global Talent Search Program",
//       },
//       {
//         item: "d. Hong Kong Digital Health Trend Survey Report",
//       },
//       {
//         item: "e. Interview Report on Opinion and Dilemma Preference Gaps among the public, government, and other stakeholders ",
//       },
//     ],
//   },
//   {
//     title: "D3. Hong Kong e-Health Blueprint",
//     contentList: [],
//   },
//   {
//     title: "D4. Risk Policy Inventory and Customized Policy Guidelines",
//     contentList: [],
//   },
//   {
//     title:
//       "D5. Risk Communication Strategy Guidelines and Communication Intervention Protocols",
//     contentList: [],
//   },
//   {
//     title:
//       "D6. Series of Public Workshops, Seminars, News Releases, and Media Coverages and PhD graduations",
//     contentList: [],
//   },
//   {
//     title: "D7. Series of Academic Papers in Journals and Conference",
//     contentList: [],
//   },
// ]);
</script>

<style lang="scss">
.deliverables-box {
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
    .list-box {
      margin-bottom: 30px;
    }
    .main-text{
      font-size: 20px;
      margin-bottom: 10px;
    }
    .list-item{
      display: flex;
      margin-bottom: 10px;
      .weight{
        font-weight: 600;
      }
      .title-num{
        width: 50px;
      }
      .text-box{
        flex: 1;
        .text-sub-1{
          margin-bottom: 5px;
        }
      }
    }
  }
}
</style>
