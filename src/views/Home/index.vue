<template>
  <header>
    <div class="nav">
      <!-- 导航前进、后退按钮 -->
      <div class="nav-to">
        <div class="back">
          <left-square-outlined :style="{ fontSize: '20px' }" />
        </div>
        <div class="to">
          <right-square-outlined :style="{ fontSize: '20px' }" />
        </div>
      </div>
      <!-- 导航 -->
      <ul class="mean">
        <li v-for="(item, index) in 3" :key="index">
          <a href="javascript:;" class="font-bold">首页</a>
        </li>
      </ul>
      <!-- 搜索框、头像 -->
      <div class="avr-inp">
        <div class="input" :class="active ? 'active' : 'color'">
          <search-outlined :style="{ color: active ? '#335eea' : '' }" />
          <a-input
            v-model:value="value"
            :bordered="false"
            placeholder="请输入"
            @focus="active = true"
            @blur="active = false"
          />
        </div>
        <div class="avatar">
          <a-avatar size="large"> </a-avatar>
        </div>
      </div>
    </div>
  </header>
  <div class="main">
    <div class="content">
      <!-- by Apple Music 部分 -->
      <MusicSection title="by Apple Music" />
      <!-- 推荐歌单 部分 -->
      <MusicSection title="推荐歌单" right />
      <!-- For You 部分 -->
      <ForYou />
      <!-- 新专速递 部分 -->
      <SingerSection title="推荐艺人" />
      <!-- 新专速递 部分 -->
      <MusicSection title="新专速递" right />
      <!-- 排行榜 部分 -->
      <MusicSection title="排行榜" right />
    </div>
  </div>
</template>
<script>
import { defineComponent, ref } from "vue";
import MusicSection from "@/components/MusicSection/index.vue";
import SingerSection from "@/components/SingerSection/index.vue";
import {
  SearchOutlined,
  LeftSquareOutlined,
  RightSquareOutlined,
  CaretRightOutlined,
  DislikeOutlined,
  StepForwardOutlined,
} from "@ant-design/icons-vue";
import { Input, Avatar } from "ant-design-vue";
import ForYou from "../../components/ForYou/index.vue";
export default defineComponent({
  components: {
    MusicSection,
    SingerSection,
    SearchOutlined,
    LeftSquareOutlined,
    RightSquareOutlined,
    CaretRightOutlined,
    DislikeOutlined,
    StepForwardOutlined,
    [Input.name]: Input,
    [Avatar.name]: Avatar,
    ForYou,
  },
  setup() {
    const value = ref("");
    const active = ref(false);
    return {
      value,
      active,
    };
  },
});
</script>
<style lang="less" scoped>
@import "./index.less";
</style>
