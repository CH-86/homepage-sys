<template>

  <div id="textbox">
    <div v-for="(devTool, index) in meineText" :key="index">
      <el-divider style="border-color: burlywood; margin: 2px 0 2px;" v-if="index"></el-divider>
      <div id="devTool">
        <div class="itemTitle">{{ devTool.title }}</div>
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
  font-size: 12px;
}
#textbox {
  border: 1px solid orange;
}

#devTool {
  display: flex;
  margin: 0 10px 0 10px;
}
.itemTitle {
  width: 42%;
  margin: 0 5px 0 5px;
}
.itemText {
  width: 58%;
  margin: 0 5px 0 5px;
}
</style>
