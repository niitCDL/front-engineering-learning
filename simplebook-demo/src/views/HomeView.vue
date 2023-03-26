<script setup>
// import TheWelcome from '../components/TheWelcome.vue'
import { onBeforeMount, ref, onMounted, reactive } from 'vue';

let content = ref(`<p class="content_text">
                      我是个爱干净的人，每天大扫除是我的习惯，可自从感染后，干净的家已面目全非。 发烧头晕乏力不想吃
                      <br/>
                      饭，这些症状的弄的人都不像人了，整天在床上躺着，牙...        
                    </p>
          `);

let content2 = ref(`<p class="content_text">
  今天，是小甜甜出生的第758天。 不曾想，我一个社恐妈妈，竟生了一个社牛宝
  <br/>宝。 在甜甜小的时候，她这一特征还不太明显，最近我带小甜甜出去散步时，...     
                    </p>
          `);

</script>

<template>
  <div class="home_container">
    <div class="content_left">
      <div style="border-bottom: 1px solid lightgray;margin-bottom: 20px;">
        <h3 style="margin-bottom: 5px;">生病后家将不家了</h3>
        <div v-html="content"></div>
        <div style="margin-bottom: 20px;">
          <span class="iconfont icon-diamond" style="color:#ea6f5a;margin-right: 10px;font-size: 14px;"> 46.6</span>
          <span style="margin-right: 10px;color:#b4b4b4;font-size: 14px;">奋发春风cw</span>
          <span class="iconfont icon-pinglun" style="color:#b4b4b4;margin-right: 10px;font-size: 14px;">32</span>
          <span class="iconfont icon-aixin" style="color:#b4b4b4;margin-right: 10px;font-size: 14px;">281</span>
        </div>
      </div>
      <div style="border-bottom: 1px solid lightgray;margin-bottom: 20px;">
        <h3 style="margin-bottom: 5px;">甜妈日记 | 甜甜有点小社牛</h3>
        <div v-html="content2"></div>
        <img src="../assets/images/person.jpg"
          style="width: 150px;float: right;position: relative;top: -80px;right: 10px;">
        <div style="margin-bottom: 20px;">
          <span class="iconfont icon-diamond" style="color:#ea6f5a;margin-right: 10px;font-size: 14px;"> 14.2</span>
          <span style="margin-right: 10px;color:#b4b4b4;font-size: 14px;">田心尔</span>
          <span class="iconfont icon-pinglun" style="color:#b4b4b4;margin-right: 10px;font-size: 14px;">14</span>
          <span class="iconfont icon-aixin" style="color:#b4b4b4;margin-right: 10px;font-size: 14px;">69</span>
        </div>
      </div>
    </div>
    <div class="content_right">
      <div>
        <img src="../assets/images/banner-daily.png" style="width: 280px;">
      </div>
      <div>
        <img src="../assets/images/banner-club.png" style="width: 280px;">
      </div>
      <div>
        <img src="../assets/images/banner-lianzai.png" style="width: 280px;">
      </div>
      <div>
        <img src="../assets/images/banner-authority.png" style="width: 280px;">
      </div>
      <div class="download_box">
        <div>
          <img src="../assets/images/download-index.png" style="width: 60px;">
        </div>
        <div style="margin-left: 30px;position: relative;top: 10px;">
          <div style="font-size: 15px;">
            <span>下载简书手机APP</span>
            <span style="position: relative; top:-2px;margin-left: 10px;">&gt;</span>
          </div>
          <div style="font-size: 13px;color: #999;margin-top: 4px;">
            随时随地发现和创新内容
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.home_container {
  display: flex;
  width: 1000px;
  height: 398px;
  /* border: 1px solid lightgray; */
  margin: 100px auto !important;
}


.content_left {
  width: 65%;
  margin-right: 30px;

  /* height: 200px;
  background-color: aqua; */
}

.content_right {
  width: 35%;
  height: 100%;
  padding-left: 30px;
  position: relative;
  top: -28px;
}

.content_text {
  margin: 0 0 8px;
  font-size: 13px;
  line-height: 24px;
  color: #999;
}

.download_box {
  cursor: pointer;
  width: 280px;
  height: 82px;
  display: flex;
  justify-content: center;
  border:1px solid lightgray;
  border-radius: 5px;
  background-color: #fff;
  margin-top: 5px;
  padding-top: 10px;
}

</style>
