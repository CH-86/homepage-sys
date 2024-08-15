<template>
  <div id="resultsList">
    <h3>&nbsp;開発実績</h3>
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
    title: '・建築資材受注発注配車システム',
    items: ['AS/400']
  },
  {
    title: '・アパレル向け販売管理システム',
    items: ['AS/400']
  },
  {
    title: '・アパレル向け経営管理システム',
    items: ['OS400', 'AS/400']
  },
  {
    title: '・短期派遣管理システム',
    items: ['NT Access2K VB']
  },
  {
    title: '・研究所用薬品管理システム',
    items: ['ColdFusion']
  },
  {
    title: '・オンライン受発注、請求、支払いシステム（EOS）',
    items: ['AS/400']
  }
])
</script>

<style scoped>
#resultsList {
  width: 380px;
  background-color: rgb(239, 239, 239);
  padding: 10px 10px 0 10px;
}
</style>
