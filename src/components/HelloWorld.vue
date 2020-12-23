<template>
  <div class="hello">
    <div class="backimg">
      <el-image class= "underground" alt="lines"
            style="width: 88vw; height: auto"
            src ="https://i.imgur.com/Dt2F7ts.jpg" 
            fit="cover"></el-image>
      <div class="whiteblock"></div>
      <el-image class= "background" alt="white back ground with word" 
            style="width: 90vw; height: auto"
            src ="https://i.imgur.com/QWUsaT6.png"
            fit="cover"></el-image>
    </div>
    <div class="content">
      <div class="headblock"></div>
      <div class="wordblock">
        <div class="wordblock_con">
          <div class="wordblock_con_1">
            <h1 class="hometitle">{{hometitle1}}</h1>
            <p class="word" 
            v-for=" (contentword) in text1"
            :key="`location-option-${contentword}`">{{contentword.p}}</p>
          </div>
        <br>
        <br>
        <br>
        <br>
        <br>

        <div class="wordblock_con_2">
          <h1 class="hometitle">{{hometitle2}}</h1>
            <p class="word gray_word">社會關懷與品格實踐能力｜美感認知與經典欣賞能力｜自然感知與創新發想能力｜邏輯思辨與語文溝通能力｜國際觀點與在地行動能力｜資訊掌握與科技應用能力</p>
            <p class="newword">{{text2_1}}</p>
            <p class="newword2">{{text2_2}}</p>
          </div>
        </div>
      <div class="separate"></div>
      <div class="big_newstitle">
              近期活動
      </div>
      <div class="news">
        
        <el-carousel :interval="4000" type="card" height="480px">
          <el-carousel-item v-for="item in newspicture" :key="item">
            <br>
            <br>
            <div class="demo-image">
              <div class="block">
                <el-image
                  style="width: 100%; height: 336px"
                  :src ="item.src"
                  fit="cover"></el-image>
              </div>
            </div>
            <p class="newstitle">{{item.title}}</p>
            <p class="newsword">{{item.word}}</p>
          </el-carousel-item>
        </el-carousel>
      </div>
      <div class="separate2"></div>
      <div class="bottomcolor">
        <div class="contect schoolname">國立清華大學藝術學院學士班</div>
        <div class="contect addr">30014新竹市南大路521號（教學大樓3F）</div>
        <div class="contect phone">+886-3-5715131 #78802 / ipta@my.nthu.edu.tw</div>
      </div>
    </div>
  </div>
  </div>
  
</template>

<script>
export default {
  name: 'hello',
  data(){
    return {
    hometitle1: "學士班特色",
    text1:[{
        p:"清華是國際頂尖科技大學，加上合校後的藝術學院，具備發展「科技藝術」的卓越條件。"
      },
      {
        p:"我們號召臺灣年輕一代的科技藝術學者專家，我們規劃有科技藝術跨域特別課程，並與業界合作推出創意跨域專題。"
      },
      {
        p:"你，不需猶豫，歡迎你的加入！"
      },
    ] ,
    hometitle2: "核心能力",
    text2_1:"清華大學2018年成立藝術學院〝科技藝術〞跨域「學士班」。「科技藝術（TechArt）」是當代藝術的新形式創作也是國際藝術發展的重要趨勢，包含虛擬藝術、互動藝術、電腦動畫、電腦音樂、聲音藝術、科技性表演藝術、混合藝術、網路社群、創客藝術、仿生藝術、生物藝術、人工生命…等。在當代數位美學與數位藝術的基礎下，我們結合創新科技，如各種互動感測技術、虛擬實境、物聯網、人工智慧、大數據分析、基因工程…，把「科技」與「藝術」結合視為「未來文化學」，培養前瞻性、跨域研究與創作人才。",
    text2_2:"因應未來產業的發展趨勢，創新科技與當代藝術結合之創作如雨後春筍。清華大學的是國內科學與科技的頂尖學府，對藝術學院發展「科技藝術」具有得天獨厚的優勢。本班師資除來自清華校內藝術學院、電資學院、工學院、生命科學院、人文社會等跨域教師外，我們也將聘進一群來自美國、歐洲與日本跨國與跨域的專業教師。也廣邀在臺灣在科技藝術創作領域最頂尖的業界團隊與藝術家加入我們的教學團隊，讓同學得到專業與多元的指導，並在共享學習、共享創意的環境裡，開創未來的產業，盡情發揮自己的潛能。",
    newspicture:[
      { src : "https://ipta.nthu.edu.tw/wp-content/uploads/2020/10/banner.png",
        title : "那顆Ｇ1咻！",
        word : " 國立清華大學藝術學院學士班第一屆系展"},
      { src : "https://ipta.nthu.edu.tw/wp-content/uploads/2019/10/board-2303325_1920.jpg",
        title : "2020藝術學院學士班春之清華獎學金",
        word : "獲獎名單"},
      { src : "https://ipta.nthu.edu.tw/wp-content/uploads/2020/05/tfho.jpg",
        title:"科技物件與人類幻象",
        word:"講座與工作坊",},
      { src : "https://ipta.nthu.edu.tw/wp-content/uploads/2020/05/200528.jpg",
        title : "Art and the Brain: A Glimpse of Neuroaesthetics從腦科學看藝術",
        word: "演講"},
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
  max-width:1430px;
  top: 0px;
  left:0px;
}

.whiteblock{
  position:absolute;
  background-color: white;
  width:40vw;
  left:0px;
  height:340%;
}

.background{
  position: absolute;
  width: 100vw;
  height:auto;
  left:0px;
  top: 20px;
}
.content {
  position: relative;
  z-index:888;
}
.headblock{
  height:110vh;
}

.wordblock{
  width:90vw;

}

.wordblock_con{
  padding-left:22%;
  width:60vw;
}

.hometitle{
  font-size:20px;
}
.word{
  line-height:20px;
  font-size:13px;
  padding:9px;
}

.separate{
  width:100%;
  height:30vh;
}
.separate2{
  background-color: white;
  width:100%;
  height:10vh;
}

.news{
  padding-top:20vh;
  padding-left:10%;
  background-color: white;
}
.el-carousel {
  width:85vw;
  max-width:1440px;
}
.el-carousel__item {
    left:4vw;
    width:551px;
    filter: blur(20px);
}
.is-active{
  filter: blur(0px);
}
.big_newstitle{
  align-items: center;
  z-index:0;
  letter-spacing: 0.5em;
  border:solid 2px #a0cccc;
  color:#a0cccc;
  padding:10px;
  padding-left:20px;
  border-radius: 10px;
  font-family: Roboto;
  font-weight: 900;
  position: absolute;
  left:75px;
  font-size:30px;
}

.newstitle{
  letter-spacing: 0.05em;
  font-family: "Gill Sans", sans-serif;
  font-weight: 700;
}
.newsword{
  color:rgb(184, 182, 182);
  font-size:12px;
}
.gray_word{
  font-size:12px;
  color:rgb(184, 182, 182);
}
.bottomcolor{
  padding-top:20px;
  left:0px;
  width:98vw;
  height:10vh;
  background-color: #a0cccc;
}
.wordblock_con_2{
  height:50vh;
}
.newword{
position: absolute;
width: 25vw;
height: 633px;
left: 23vw;
top: 168vh;
font-size: 13px;
line-height: 40px;
text-align: center;
letter-spacing: 0.05em;
text-transform: uppercase;
}
.newword2{
position: absolute;
width: 25vw;
height: 633px;
left: 51vw;
top: 168vh;
font-size: 13px;
line-height: 40px;
text-align: center;
letter-spacing: 0.05em;
text-transform: uppercase;
}

.contect{
  position:absolute;
  width:20vw;
  font-size:12px;
}
.addr{
  padding-left:60vw;
}
.phone{
  padding-left:77vw;
}
</style>