<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <div class="head">
      <div id="leftArea">
        <div id="logo">
          <img class="logo" src="https://www.sts-co.jp/img/logo.gif" width="130" height="130" />
        </div>
        <div class="wrapper">
          <nav>
            <RouterLink to="/">Home</RouterLink>
            <RouterLink to="/about">会社概要</RouterLink>
            <RouterLink to="/dev">開発環境</RouterLink>
            <RouterLink to="/results">開発実績</RouterLink>
            <RouterLink to="/recruit">採用情報</RouterLink>
          </nav>
        </div>
      </div>
      <div>
        <div id="rightArea">
          <div>
            <a href="/"><img src="https://www.sts-co.jp/img/home.gif" alt="/" /></a>
            <a href="mailto:naito@sts-co.jp"
              ><img src="https://www.sts-co.jp/img/contact.gif" alt="/"
            /></a>
          </div>
          <div>
            <img src="https://www.sts-co.jp/img/hotline.gif" alt="/" />
            <img src="https://www.sts-co.jp/img/company.jpg" alt="/" width="380px" height="100px" />
          </div>
        </div>
      </div>
    </div>
  </header>
  <body>
    <div class="container">
      <RouterView />
    </div>
  </body>
  <footer>
    <div class="footBand">
      <div>
        ©2009 STS Co., Ltd. All rights Reserved;
        <RouterLink to="/about">個人情報保護基本方針</RouterLink>
      </div>
    </div>
  </footer>
</template>

<style scoped>
#leftArea {
  width: 380px;
}
#rightArea {
  vertical-align: top;
  text-align: -webkit-right;
  width: 380px;
  height: 160px;
  background-color: rgb(243, 243, 243);
}

body {
  display: flex;
  justify-content: center;
}

.head {
  display: flex;
  justify-content: center;
}
footer {
  display: flex;
  justify-content: center;
}
.footBand {
  width: 760px;
  font-size: 13px;
  padding: 5px 0 5px 0;
  background-color: #b29f77;
  color: white;
}

#logo {
  width: 354px;
  text-align: -webkit-center;
  background-color: rgb(255, 255, 255);
}

.container {
  width: 760px;
  display: flex;
  justify-content: center;
}
</style>
