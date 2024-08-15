<template>
  <div id="recruitList">
    <h3>&nbsp; 採用情報</h3>
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
  {
    title: '募集人員',
    items: [
      'システムエンジニア',
      '◆ System i5(AS/400)',
      '◆ 汎用',
      '上記いずれかの開発経験が１年以上の方(未経験者可)'
    ]
  },
  {
    title: '東京都',
    items: ['東京都']
  },
  {
    title: '勤務時間',
    items: ['始業　9:00　～　終業　18:00', '標準実労時間/1日8時間']
  },
  {
    title: '諸手当',
    items: ['交通費全額支給(上限5万円)、管理職手当てなど']
  }
])
</script>

<style scoped>
#recruitList {
  width: 380px;
  background-color: rgb(239, 239, 239);
  padding: 10px 10px 0 10px;
}
</style>
