<template>
  <div style="width: 100%">
    <el-descriptions>
      <el-descriptions-item label="弊社担当"
        >内藤 照雄
        <a href="/">&lt;naito@sts-co.jp&gt;</a>
      </el-descriptions-item>
    </el-descriptions>
    <div class="context">お問い合わせ内容</div>
    <div class="mb-2 ml-4">
      <el-radio-group v-model="radio1">
        <el-radio value="1" size="small"> 業務システム開発 </el-radio>
        <el-radio value="2" size="small"> Webシステム開発 </el-radio>
        <el-radio value="3" size="small"> 技術者派遣 </el-radio>
        <el-radio value="4" size="small"> Webデザイン </el-radio>
        <el-radio value="5" size="small"> システムコンサルティング </el-radio>
        <el-radio value="6" size="small"> その他 </el-radio>
      </el-radio-group>
    </div>
    <div class="context">&lt;詳細&gt;</div>
    <div class="context">
      <el-input v-model="textarea" style="width: 240px" :rows="2" type="textarea" />
    </div>
    <div class="context">ご連絡先</div>
    <div class="context">
      <el-form
        :model="form"
        label-width="auto"
        style="max-width: 300px"
        label-position="left"
        size="small"
      >
        <el-form-item label="企業名">
          <el-input v-model="form.kigyou" />
        </el-form-item>
        <el-form-item label="ご担当の方	">
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
        <el-form-item label="URL">
          <el-input v-model="form.url" />
        </el-form-item>
        <el-form-item>
          <el-button type="info" @click="onSubmit">送信</el-button>
        </el-form-item>
      </el-form>
    </div>
  </div>
</template>
<script lang="ts" setup>
import { ref, reactive } from 'vue'
const radio1 = ref('')
const textarea = ref('')
const form = reactive({
  kigyou: '',
  tantou: '',
  resource: '',
  phonenumber: '',
  url: '',
  email: ''
})
const onSubmit = () => {
  console.log(form)
}
</script>
