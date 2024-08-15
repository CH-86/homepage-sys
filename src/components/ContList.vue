<template>
  <div>
    <div class="contents">Contents Of Service</div>
    <div class="contList">
      <p v-for="(item, index) in items" :key="index">{{ index }}.{{ item }}</p>
      <a href="" target="_blank" one-link-mark="yes" style="color: blue">
        &nbsp;m-Doc（エム－ドック）
      </a>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
const items = ref([
  'コンピュータシステムの受託開発',
  'コンピュータシステムのｱｳﾄｿｰｼﾝｸﾞ',
  'コンピュータのパッケージサービス',
  'コンピュータに関するコンサルティング',
  'コンピュータ技術者の派遣',
  'メンタルヘルス事業'
])
</script>

<style>
.contList {
  width: 370px;
  font-size: 10pt;
  padding: 5pt;
  line-height: 120%;
  border-style: solid;
  border-color: #cccccc;
}
.contents {
  display: flex;
  justify-content: center;
}
</style>
