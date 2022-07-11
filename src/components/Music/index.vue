<template>
  <a href="javascript:;" class="list">
    <div class="img_content">
      <div class="button">
        <caret-right-outlined :style="{ fontSize: '30px', color: 'white' }" />
      </div>
      <div class="img">
        <img
          src="https://p1.music.126.net/cPaBXr1wZSg86ddl47AK7Q==/109951165375130918.jpg"
          alt=""
        />
      </div>
      <div class="img-filter">
        <img
          src="https://p1.music.126.net/cPaBXr1wZSg86ddl47AK7Q==/109951165375130918.jpg"
          alt=""
        />
      </div>
    </div>
    <div class="text">
      <p class="font-bold">Happy Hits</p>
      <p>by Apple Music</p>
    </div>
  </a>
</template>
<script>
import { defineComponent } from "vue";
import { CaretRightOutlined } from "@ant-design/icons-vue";
export default defineComponent({
  components: {
    CaretRightOutlined,
  },
});
</script>
<style lang="less" scoped>
@import "./index.less";
</style>
