<template>
  <div id="app">
    <div id="nav">
      <el-menu
      :default-active="activeIndex"
      class="el-menu-demo"
      mode="horizontal"
      @select="handleSelect"      
      text-color=":#0f161d"
      active-text-color=" #a0cccc">
        <el-menu-item index="1"><router-link to="/">藝術學院學士班</router-link> </el-menu-item>
        <el-menu-item index="2"><router-link to="/about">NEWS</router-link> </el-menu-item>
        <el-submenu index="3">
          <template slot="title">ABOUT</template>
          <el-menu-item class="item_in_submenu" index="3-1"><router-link to="/about">簡介</router-link></el-menu-item>
          <el-menu-item class="item_in_submenu" index="3-2"><router-link to="/about">課程</router-link></el-menu-item>
          <el-menu-item class="item_in_submenu" index="3-3"><router-link to="/about">國際交換</router-link></el-menu-item>
          <el-menu-item class="item_in_submenu" index="3-4"><router-link to="/about">藝術學院大樓</router-link></el-menu-item>
          <el-menu-item class="item_in_submenu" index="3-5"><a href="https://www.facebook.com/清華大學藝術學院學士班-1103816213137155/?modal=admin_todo_tour">FB</a></el-menu-item>
        </el-submenu>
        <el-submenu index="4">
          <template slot="title">招生</template>
          <el-submenu class="item_in_submenu" index="4-1">
            <template class="item_in_submenu" slot="title">招生資料</template>
            <el-menu-item class="item_in_submenu" index="4-1-1">2020</el-menu-item>
            <el-menu-item class="item_in_submenu" index="4-1-2">2019</el-menu-item>
            <el-menu-item class="item_in_submenu" index="4-1-3">2018</el-menu-item>
          </el-submenu>
          <el-menu-item index="4-2"><router-link to="/about">Q and A</router-link></el-menu-item>
        </el-submenu>
        <el-submenu index="5">
          <template slot="title">師資</template>
          <el-menu-item class="item_in_submenu" index="2-1"><router-link to="/about">學士班</router-link></el-menu-item>
          <el-menu-item class="item_in_submenu" index="2-2"><router-link to="/about">藝社系</router-link></el-menu-item>
          <el-menu-item class="item_in_submenu" index="2-3"><router-link to="/about">音樂系</router-link></el-menu-item>
          <el-menu-item class="item_in_submenu" index="2-4"><router-link to="/about">電資學院</router-link></el-menu-item>
        </el-submenu>
        <el-submenu index="6">
          <template slot="title">科技藝術</template>
          <el-menu-item class="item_in_submenu" index="6-1"><router-link to="/about">數位文創作品</router-link></el-menu-item>
          <el-menu-item class="item_in_submenu" index="6-2"><router-link to="/about">互動藝術作品</router-link></el-menu-item>
          <el-menu-item class="item_in_submenu" index="6-3"><router-link to="/about">動力藝術作品</router-link></el-menu-item>
          <el-menu-item class="item_in_submenu" index="6-4"><router-link to="/about">聲音藝術作品</router-link></el-menu-item>
          <el-menu-item class="item_in_submenu" index="6-5"><router-link to="/about">科技藝術表演</router-link></el-menu-item>
        </el-submenu>
      </el-menu>
    </div>
    <router-view/>
  </div>
  
</template>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-size:16px;
  text-align: center;
  color: #0f161d;
}

#nav {
  padding: 0px;
  position:fixed;
  top:-8px;
  left:-8px;
  z-index:9999;
}

#nav a{
    color: #0f161d;
}

#nav a.router-link-exact-active {
  color: #a0cccc;
}
a:-webkit-any-link {
  color:#0f161d;
  text-decoration-line: unset;
}
.el-menu-demo{
  width:100vw;
}
.item_in_submenu{
  font-size:12px;
}
</style>