<script setup>
import ContList from '../components/ContList.vue'
import TextBox from '../components/TextBox.vue'
import { ref, reactive } from 'vue'
const info = reactive({
  name: '',
  phonenumber: '',
  email: ''
})
const onSubmit = () => {
  console.log(info)
}
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
  },
  {
    title: '昇給',
    items: ['年1回(4月)']
  },
  {
    title: '賞与',
    items: ['年2回(夏季・年末)　※業績によっては決算賞与の支給もあり']
  },
  {
    title: '社会保険',
    items: ['厚生年金・雇用保険・労災保険・健康保険']
  },
  {
    title: '健保組合',
    items: ['政府管掌']
  },
  {
    title: '応募方法',
    items: ['１.右記フォームから連絡先をお知らせください。折り返しご連絡申し上げます。',
     '２.前もって実務経歴書と履歴書を郵送またはメールで送っていただくことも可能です。',
     '＜送付先＞ 110-0015東京都台東区東上野１-２４-２ 山茂ビル ２F',
     '株式会社エス・ティ・エス',
     '採用担当　宛',
     '＜連絡先＞',
    'TEL：03-5807-8691/FAX：03-5807-8692',
    'MAIL：saiyo@sts-co.jp'
    ]
  },
])
</script>

<template>
  <div id="recruitList">
    <h3>&nbsp; 採用情報</h3>
    <TextBox :meineText="devTools" />
  </div>
  <div style="width: 380px">
    <ContList />
    <!-- <ContentsOfService /> -->
    <div id="recruitBox">
      <span> 当社に応募される方は、連絡先を送信してください。</span>
      <span> 折り返しご連絡申し上げます。</span>
      <div class="recruitForm">
        <div class="recruitLabel">
          <span>氏名</span>
          <span>電話番号</span>
          <span>E-Mail </span>
        </div>
        <div class="recruitInput">
          <el-input v-model="info.name" style="width: 140px" size="small"/>
        <el-input v-model="info.phonenumber" style="width: 140px" size="small"/>
        <el-input v-model="info.email" style="width: 140px" size="small"/>
      </div>

        </div>
        <div>
          <el-form-item>
          <el-button type="info" @click="onSubmit">送信</el-button>
        </el-form-item>
        </div>
    </div>
  </div>
</template>

<style scoped>
#recruitList {
  width: 380px;
  background-color: rgb(239, 239, 239);
  padding: 10px 10px 0 10px;
}

#recruitBox{
  display: flex;
  flex-direction: column;
  align-items: center; 
  height: 300px;
  padding: auto;
}

.recruitForm{
  display: flex;
  text-align: center;
}
.recruitLabel{
  display: flex;
  flex-direction: column;
  text-align: left;
  margin-top: 5px;
  margin-bottom: 5px;
  width: 70px;
}
.recruitInput{
  display: flex;
  flex-direction: column;
  margin-top: 5px;
  margin-bottom: 5px;
}
</style>
