<template>
  <div class="apple_music">
    <div class="header">
      <h2 class="font-bold">{{ title }}</h2>
      <a href="javascript:;" v-if="right">查看更多</a>
    </div>
    <div class="apple_list">
      <Music v-for="(item, index) in 5" :key="index" />
    </div>
  </div>
</template>
<script>
import { defineComponent } from "vue";
import Music from "../Music/index.vue";
export default defineComponent({
  components: {
    Music,
  },
  props: {
    title: {
      type: String,
      required: true,
    },
    right: {
      type: Boolean,
      default: false,
    },
  },
});
</script>
<style lang="less" scoped>
@import "./index.less";
</style>
