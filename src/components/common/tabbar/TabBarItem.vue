<template>
  <div class="tab-bar-item">
    <div v-if="!isActive"><slot name="item-icon"></slot></div>
    <div v-else><slot name="item-icon-active"></slot></div>
    <div :class="{ active: isActive }"><slot name="item-text"></slot></div>
    <!-- <img src="../../assets/img/tabbar/home.png" alt="" />
    <div>首页</div> -->
  </div>
</template>

<script>
export default {
  data() {
    return {
      isActive: true,
    };
  },
};
</script>

<style>
.tab-bar-item {
  flex: 1;
  text-align: center;
  height: 49px;
  font-size: 14px;
}
.tab-bar-item img {
  width: 24px;
  margin-top: 3px;
  vertical-align: middle;
  margin-bottom: 2px;
}
.active {
  color: #7a7af9;
}
</style>
