<template>
  <div class="for-you">
    <h2 class="font-bold">For You</h2>
    <div class="cont-for-you">
      <div class="tui-j">
        <img
          src="https://p2.music.126.net/QxJA2mr4hhb9DZyucIOIQw==/109951165422200291.jpg?param=1024y1024"
          alt=""
        />
        <div class="tui-j-con">
          <div class="text font-bold">
            <p>每日</p>
            <p>推荐</p>
          </div>
          <div class="button">
            <caret-right-outlined
              :style="{ fontSize: '30px', color: 'white' }"
            />
          </div>
        </div>
      </div>
      <div class="FM">
        <img
          src="https://p2.music.126.net/QxJA2mr4hhb9DZyucIOIQw==/109951165422200291.jpg?param=1024y1024"
          alt=""
        />
        <div class="FM-con">
          <img
            src="https://p3.music.126.net/JOJvZc_7SqQjKf8TktQ_bw==/29686813951246.jpg?param=512y512"
            alt=""
          />
          <div class="text">
            <div class="name">
              <p class="font-bold">误会的一生</p>
              <a class="font-bold">Beyond</a>
            </div>
            <div class="icon">
              <dislike-outlined :style="{ fontSize: '30px', color: 'white' }" />
              <caret-right-outlined
                :style="{ fontSize: '30px', color: 'white' }"
              />
              <step-forward-outlined
                :style="{ fontSize: '30px', color: 'white' }"
              />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import { defineComponent } from "vue";
import {
  CaretRightOutlined,
  DislikeOutlined,
  StepForwardOutlined,
} from "@ant-design/icons-vue";
export default defineComponent({
  components: {
    CaretRightOutlined,
    DislikeOutlined,
    StepForwardOutlined,
  },
});
</script>
<style lang="less" scoped>
@import "./index.less";
</style>
