<template>
  <!-- <h1>23243</h1> -->
  <div id="textbox">
    <div v-for="(devTool, index) in meineText" :key="index">
      <el-divider style="border-color: burlywood" v-if="index"></el-divider>
      <div id="devTool">
        <div class="itemText">{{ devTool.title }}</div>
        <div class="itemText">
          <p v-for="item in devTool.items" :key="item">{{ item }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
interface MeineText {
  title: string
  items: string[]
}

const props = defineProps<{
  meineText: MeineText[]
}>()
</script>

<style>
#textbox div {
  min-width: 80px;
  font-size: 14px;
}
#textbox {
  border: 1px solid orange;
}

#devTool {
  display: flex;
  margin: 0 10px 0 10px;
}
.itemText {
  margin: 0 10px 0 10px;
}
</style>
