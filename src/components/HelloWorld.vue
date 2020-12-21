<template>
  <div class="hello">
    <div class="backimg">
      <img class= "underground" alt="lines" src="https://i.imgur.com/0mAK5Pv.jpg">
      <img class= "background" alt="white back ground with word" src="https://i.imgur.com/fPwm7R4.png">
    </div>
    <div class="content">
      <div class="wordblock">
        <h1 class="title">{{title}}</h1>
        <p class="word" 
        v-for="(p) in text"
        :key="`location-option-${p}`">{{p.p}}</p>
      </div>
      <div class="news">
        <el-carousel :interval="4000" type="card" height="200px">
          <el-carousel-item v-for="item in newspicture" :key="item">
            <div class="imgurblock">
              <img class="newsimgur" :src="item.src">
            </div>
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
      {src : "https://ipta.nthu.edu.tw/wp-content/uploads/2020/10/banner.png"},
      {src : "https://ipta.nthu.edu.tw/wp-content/uploads/2020/09/light2-01.jpg"},
      {src : "https://ipta.nthu.edu.tw/wp-content/uploads/2019/10/board-2303325_1920.jpg"},
      {src : "https://ipta.nthu.edu.tw/wp-content/uploads/2020/05/tfho.jpg"},
      {src : "https://ipta.nthu.edu.tw/wp-content/uploads/2020/05/200528.jpg"},
      {src : "https://ipta.nthu.edu.tw/wp-content/uploads/2020/04/NEWS.jpg"}
    ],
    
    }
  },

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.backimg{
  z-index: 1;
}
.underground{
position: fixed;
width: 120%;
height:auto;
left: -110px;
top: 70px;
}

.background{
  position: absolute;
  width: 100%;
  height:auto;
  left: 0px;
  top: 60px;
}
.content {
  position: relative;
  z-index:9999;
  top:100;
}
.wordblock{
  top:1000px;
}
.title{
  font-size:20px;
}
.word{
  line-height:20px;
  font-size:12px;
}

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
.news{
  height:100vh;
  width:100vw;
}
  
.el-carousel__item {
    color: #475669;
    font-size: 14px;
    opacity: 0.75;
    line-height: 200px;
    margin: 0;
    width:60vw;
    height:1100px;
    text-align: center;
}
.newsimgur{
  text-align: center;
  width:100%;
  height:auto;
}
.newsimgur{
  height:100%;
  background-color: red;
  padding:10px;
}
</style>