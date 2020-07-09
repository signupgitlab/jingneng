<template>
  <div class="cash_flow">
    <div class="title_box">
      <img class="title" src="../../static/images/xjllfx.png" alt="">
      <img class="ico" src="../../static/images/ae.png" alt="">
    </div>
    <div class="change_box">
      <button @click="change('tab_1')" :class="nowActive === 'tab_1' ? 'active' : ''">本周</button>
      <button @click="change('tab_2')" :class="nowActive === 'tab_2' ? 'active' : ''">本月</button>
    </div>
    <div class="chart_box"></div>
  </div>
</template>
<script>
export default {
  name: 'cashFlow',
  data() {
    return {
      nowActive: 'tab_1',
    }
  },
  methods: {
    change(nowVal) {
      this.nowActive = nowVal
    }
  },
}
</script>
<style lang="scss" scoped>
@import '@/assets/css/rem.scss';

.cash_flow {
  flex: none;
  height: 35%;
}
</style>