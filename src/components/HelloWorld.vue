<template>
  <div class="hello">
    
    <div class="backimg">
      <img class= "underground" alt="lines" src="https://i.imgur.com/0mAK5Pv.jpg">
      <img class= "background" alt="white back ground with word" src="https://i.imgur.com/fPwm7R4.png">
    </div>
    <div class="wordblock">
      <h1 class="title">{{title}}</h1>
      <p class="word" 
      v-for="(p) in text"
      :key="`location-option-${p}`">{{p.p}}</p>
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
width: 105vw;
height:auto;
left: -110px;
top: 10px;
}

.background{
  position: absolute;
  width: 100%;
  height:auto;
  left: 0px;
  top: 0px;
}
.wordblock{
  top:50vh;
  position:relative;
  z-index:9999;
}
.title{
  font-size:20px;
}
.word{
  line-height:20px;
  font-size:12px;
}
</style>