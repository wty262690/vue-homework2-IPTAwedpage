<template>
  <div class="hello">
    <div class="backimg">
      <img class= "underground" alt="lines" src="https://i.imgur.com/0mAK5Pv.jpg">
      <img class= "background" alt="white back ground with word" src="https://i.imgur.com/fPwm7R4.png">
    </div>
    <div class="content">
      <div class="headblock"></div>
      <div class="wordblock">
        <h1 class="title">{{title}}</h1>
        <p class="word" 
        v-for="(p) in text"
        :key="`location-option-${p}`">{{p.p}}</p>
      </div>
      <div class="news">
        <el-carousel :interval="4000" type="card" height="290px">
          <el-carousel-item v-for="item in newspicture" :key="item">
            <div class="demo-image">
              <div class="block">
                <el-image
                  style="width: 100%; height: 200px"
                  :src ="item.src"
                  fit="cover"></el-image>
              </div>
            </div>
            <p class="newstitle">{{item.title}}</p>
            <p class="newsword">{{item.word}}</p>
          </el-carousel-item>
        </el-carousel>
      </div>
  </div>
  </div>
  
</template>

<script>
export default {
  name: 'hello',
  data(){
    return {
    title: "學士班特色",
    text:[{
        p:"清華是國際頂尖科技大學，加上合校後的藝術學院，具備發展「科技藝術」的卓越條件。"
      },
      {
        p:"我們號召臺灣年輕一代的科技藝術學者專家，我們規劃有科技藝術跨域特別課程，並與業界合作推出創意跨域專題。"
      },
      {
        p:"你，不需猶豫，歡迎你的加入！"
      },
    ] ,
    newspicture:[
      { src : "https://ipta.nthu.edu.tw/wp-content/uploads/2020/10/banner.png",
        title : "《那顆Ｇ1咻！》國立清華大學藝術學院學士班第一屆系展",
        word : " 「當藝術碰撞科技，會迸出什麼樣的火花呢?」"},
      { src : "https://ipta.nthu.edu.tw/wp-content/uploads/2019/10/board-2303325_1920.jpg",
        title : "2020藝術學院學士班春之清華獎學金",
        word : "【獲獎名單】"},
      { src : "https://ipta.nthu.edu.tw/wp-content/uploads/2020/05/tfho.jpg",
        title:"《科技物件與人類幻象》",
        word:"【講座與工作坊】",},
      { src : "https://ipta.nthu.edu.tw/wp-content/uploads/2020/05/200528.jpg",
        title : "Art and the Brain: A Glimpse of Neuroaesthetics從腦科學看藝術",
        word: "【演講】"},
    ],
    
    }
  },

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
}
#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

.backimg{
  z-index: 1;
}
.underground{
  position: fixed;
  width: 100%;
  max-width:1440px;
  top: 70px;
  left:0px;
}

.background{
  position: absolute;
  width: 100%;
  max-width:1440px;
  height:auto;
  left:0px;
  top: 60px;
}
.content {
  position: relative;
  z-index:888;
}
.headblock{
  height:100vh;
}

.title{
  font-size:20px;
}
.word{
  line-height:20px;
  font-size:12px;
  padding:9px;
}
.news{
  position:relative;
  left:20vw;
}
.el-carousel {
  width:65vw;
  max-width:1440px;
}
.el-carousel__item {
    width:30vw;
    filter: blur(20px);
}
.is-active{
  filter: blur(0px);
}
.newstitle{
  font-size:16px;
}

</style>