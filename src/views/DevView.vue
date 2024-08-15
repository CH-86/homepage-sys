<template>
  <div id="devList">
    <h3>&nbsp;開発環境</h3>
    <!-- <div id="textbox">
      <div v-for="(devTool, index) in devTools" :key="index">
        <el-divider style="border-color: burlywood" v-if="index"></el-divider>
        <div id="devTool">
          <div class="itemText">{{ devTool.title }}</div>
          <div class="itemText">
            <p v-for="item in devTool.items" :key="item">{{ item }}</p>
          </div>
        </div>
      </div>
    </div> -->
    <TextBox :meineText="devTools" />
  </div>
  <div style="width: 380px">
    <ContList />
    <ContentsOfService />
  </div>
</template>

<script setup>
import ContList from '../components/ContList.vue'
import ContentsOfService from '../components/ContentsOfService.vue'
import TextBox from '../components/TextBox.vue'
import { ref } from 'vue'
const devTools = ref([
  { title: '言 語', items: ['RPG', 'COBOL', 'Perl', 'PHP', 'JAVA, JSP', 'VB', '.net'] },
  { title: 'Ｄ Ｂ', items: ['DB2', 'ORACLE', ' SQL-SERVER', 'MySQL', 'PostgreSQL'] },
  { title: 'Ｏ Ｓ', items: ['OS400', ' Windows 10/7', ' Windows 2003Server', ' Solaris, Linux'] },
  { title: '開発ツール', items: ['GeneXus'] }
])
</script>

<style scoped>
#devList {
  width: 380px;
  background-color: rgb(239, 239, 239);
  padding: 10px 10px 0 10px;
}
</style>
