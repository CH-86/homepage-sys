<template>
  <el-card>
    <h2>Company Information</h2>
    <el-row>
      <el-col :span="8"><strong>Name:</strong></el-col>
      <el-col :span="16">STS Co., Ltd.</el-col>
    </el-row>
    <el-row>
      <el-col :span="8"><strong>Founded:</strong></el-col>
      <el-col :span="16">1951</el-col>
    </el-row>
    <el-row>
      <el-col :span="8"><strong>CEO:</strong></el-col>
      <el-col :span="16">Taro Yamada</el-col>
    </el-row>
    <!-- 其他公司信息 -->
  </el-card>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'CompanyInfo'
})
</script>

<style scoped>
h2 {
  margin-bottom: 20px;
}
</style>
