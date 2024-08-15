<template>
  <div><img src="https://www.sts-co.jp/img/m-doc_logo.jpg" alt="" /></div>
  <div>
    <el-text class="context" type="danger">急募案件情報</el-text>
    <el-text class="context" type="info"
      >ご希望の案件をチェックし、ご連絡先を送信してください。
    </el-text>
    <el-text class="context" type="info">(複数選択可) </el-text>
  </div>
  <div id="checkbox1">
    <el-checkbox v-model="checked1">技術者募集</el-checkbox>
  </div>
  <div id="labelText">
    <div style="width: 80px; display: flex; align-items: center; text-align: center">
      要件・備考
    </div>
    <div>
      System i5(AS/400)の技術者<br />
      Notes Dominoの技術者<br />
      ASP,PHP,Java,C,C#,C++,.NET,VB等の技術者
    </div>
  </div>
  <div class="context ApplyForm">
    <el-form
      :model="form"
      label-width="auto"
      style="max-width: 300px"
      label-position="left"
      size="small"
    >
      <el-form-item label="お名前">
        <el-input v-model="form.kigyou" />
      </el-form-item>
      <el-form-item label="ふりがな">
        <el-input v-model="form.tantou" />
      </el-form-item>
      <el-form-item label="ご希望連絡方法	">
        <el-radio-group v-model="form.resource">
          <el-radio value="phone">電話</el-radio>
          <el-radio value="mail">Mail</el-radio>
          <el-radio value="">どちらでもかまわない</el-radio>
        </el-radio-group>
      </el-form-item>
      <el-form-item label="電話" v-if="form.resource != 'mail'">
        <el-input v-model="form.phonenumber" />
      </el-form-item>
      <el-form-item label="E-Mail" v-if="form.resource != 'phone'">
        <el-input v-model="form.email" />
      </el-form-item>
      <el-form-item>
        <el-button type="info" @click="onSubmit"></el-button>
      </el-form-item>
    </el-form>
  </div>
</template>

<script setup>
import { reactive } from 'vue'
const form = reactive({
  kigyou: '',
  tantou: '',
  resource: '',
  phonenumber: '',
  email: ''
})
const onSubmit = () => {
  console.log(form)
}
</script>
<style>
#checkbox1 {
  background: #eedddd;
  padding: 1px 0 1px 5px;
}
#labelText {
  display: flex;
  border: 1px solid rgb(152, 152, 152);
}
.ApplyForm {
  width: 100%;
  height: 280px;
  margin: 10px 10px 10px 0;
  border: 1px solid rgb(152, 152, 152);
  padding: 10px 10px 10px 10px;
}
</style>
