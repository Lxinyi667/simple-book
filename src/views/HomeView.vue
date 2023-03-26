<script setup>

import TodoItem from '@/components/TodoItem.vue'
import { reactive } from 'vue'

const items = reactive([
  {
    id: 1,
    title: '活着',
    msg:'老爸隔壁床，是个93岁的老头儿，听说退休前是个局长。 他听力不好，得了病坚决不入院，儿子在纸上写了一行字给他看：“不去医院你会死！” 老头儿看完..',
    logo:'./src/assets/images/love1.png',
    date: '2023-03-24',
    finished: false,
  },
  {
    id: 2,
    title: '同事抑郁了',
    msg:'我的同事名牌大学毕业，在单位属中层领导，父母健康，孩子省心，老婆贤惠，他竟然抑郁了，原因是自己觉得什么也干不了。 昨天，接到同事电话，他说姐你在...',
    logo:'./src/assets/images/love2.png',
    date: '2023-03-23',
    finished: false,
  },
  {
    id: 3,
    title: '适合自己的就好',
    msg:'朋友说她阳了又遇上大姨妈，于是发红包让她老公下班的时候带包卫生巾回来。 我好奇地问：为啥你买东西还要给老公钱，而且他还拿了？ 朋友很自然地反问：...',
    logo:'./src/assets/images/love4.png',
    date: '2023-03-23',
    finished: false,
  },
  {
    id: 3,
    title: '至今让我后悔的一件事',
    msg:'二十多年前，我刚毕业，还没男朋友。 闺蜜经别人介绍认识了一个乡政府上班的大学生，那大学生也是刚毕业，白白净净，他老爹是退休老师，有退休金，闺蜜很...',
    logo:'./src/assets/images/love3.png',
    date: '2023-03-23',
    finished: false,
  },
])
</script>

<template>
 
  <div class="layout">
    <div v-for="item in items" :key="item.id">
      <TodoItem :item="item" />
    </div>
    <div class="bo1">
    <!-- 右边Board -->
      <div class="board">
                  <a target="_blank" href="/mobile/campaign/day_by_day/join?from=home">
                      <img referrerpolicy="no-referrer" src="https://cdn2.jianshu.io/assets/web/banner-s-daily-e6f6601abc495573ad37f2532468186f.png" alt="Banner s daily">
                  </a>
                  <a target="_blank" href="/mobile/club">
                    <img referrerpolicy="no-referrer" src="https://cdn2.jianshu.io/assets/web/banner-s-club-aa8bdf19f8cf729a759da42e4a96f366.png" alt="Banner s club">
                  </a>
                  <a utm_medium="index-banner-s" target="_blank" href="/mobile/books?category_id=284">
                    <img referrerpolicy="no-referrer" src="https://cdn2.jianshu.io/assets/web/banner-s-7-1a0222c91694a1f38e610be4bf9669be.png" alt="Banner s 7">
                  </a>
                  <a utm_medium="index-banner-s" target="_blank" href="/publications">
                    <img referrerpolicy="no-referrer" src="https://cdn2.jianshu.io/assets/web/banner-s-5-4ba25cf5041931a0ed2062828b4064cb.png" alt="Banner s 5">
                  </a>
                  
      </div>
      <!--  -->
      <a id="index-aside-download-qrbox" class="col-xs-8 download" data-toggle="popover" data-placement="top" data-html="true" data-trigger="hover" data-content="<img src=&quot;https://cdn2.jianshu.io/assets/web/download-index-side-qrcode-bef8a3919bdba9e8d965956b37291e98.png&quot; alt=&quot;Download index side qrcode&quot; />" href="/apps?utm_medium=desktop&amp;utm_source=index-aside-click" data-original-title="" title="">
        <img referrerpolicy="no-referrer" class="qrcode" src="https://cdn2.jianshu.io/assets/web/download-index-side-qrcode-bef8a3919bdba9e8d965956b37291e98.png" alt="Download index side qrcode">
        <div class="info">
          <div class="title">下载简书手机App<i class="iconfont ic-link"></i></div>
          <div class="description">随时随地发现和创作内容</div>
        </div>
      </a>
      
      <!--  -->
  </div>
  </div>
</template>
<style scoped>
*{
  margin: 0;
  padding: 0;
  background-color: #FFFFFF;
  list-style: none;
  text-decoration: none;
}
.layout {
  width: 90%;
  flex-direction: column;
  display: flex;

}
.layout div {
  flex-direction: column;

  flex: 1 ;
}

.board{

  
  display: flex;
  /* position: relative; */
  float: right;
  margin-top: -820px;
  margin-right: -60px;
  flex-direction: column;
}
.board img{
  height: 50px;
}
#index-aside-download-qrbox{
    line-height: 1.42857;
    font-size: 17px;
    font-family: -apple-system,SF UI Text,Arial,PingFang SC,Hiragino Sans GB,Microsoft YaHei,WenQuanYi Micro Hei,sans-serif;
    box-sizing: border-box;
    text-decoration: none;
    color: #333;
    cursor: pointer;
  
    min-height: 1px;
    float: right;
    margin-top: -600px;
    margin-right: -60px;
    
    padding: 5px 10px;
   
    border: 1px solid #f0f0f0;
    border-radius: 6px;
    background-color: #fff;
}
.qrcode {
    width: 60px;
    height: 60px;
    opacity: .85;
}
img {
    vertical-align: middle;
}
img {
    border: 0;
}
.info {
    display: inline-block;
    vertical-align: middle;
    margin-left: 7px;
}
</style>

