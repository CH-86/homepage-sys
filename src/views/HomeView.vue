<script setup lang="ts">
import { ref } from 'vue'
import ContList from '../components/ContList.vue'
import ApplyForm from '../components/ApplyForm.vue'

const items = ref([
  {
    title: 'AS/400開発',
    text: '  当社はSystem i5(AS/400)を中心とした基幹システムの構築を数多く行ってまいりました。当社ではAS/400発売以前のS/36,S/38からの技術を有し、さらに社内に保有するAS/400を活用し、常に新しい技術をFollow UPします。'
  },
  {
    title: 'オープン系Webアプリケーション開発',
    text: '  AS/400の開発で培った「安定性・安全性・安心感」を備えた基幹システム開発技術を、最先端のITスキルサービスのご提供に活用し、オブジェクト指向設計によるオープン系Webアプリケーション開発を行います。'
  },
  {
    title: 'ビジネスパートナー募集',
    text: '  ソフトウェア開発、構築、保守・運用業務等において、ご協力いただけるパートナー企業様を随時募集しております。'
  }
])
</script>

<template>
  <div class="mainNote">
    <div>
      <img alt="システムトータルサービス" src="https://www.sts-co.jp/img/company_profile01.jpg" />
    </div>
    <div v-for="item in items" :key="item.title">
      <div class="itemtitle">{{ item.title }}</div>
      <div class="itemtext">{{ item.text }}</div>
    </div>
  </div>
  <div style="width: 380px">
    <ContList />
    <ApplyForm />
  </div>
</template>

<style>
.mainNote {
  background-color: #fff;
  width: 380px;
}
.itemtitle {
  background-color: #3953a4;
}
.itemtext {
  text-indent: 1em;
}
</style>
