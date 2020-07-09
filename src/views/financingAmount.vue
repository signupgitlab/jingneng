<template>
  <div class="financing_amount">
    <div class="title_box">
      <img class="title" src="../../static/images/rzjejcbfx.png" alt="">
      <img class="ico" src="../../static/images/ae.png" alt="">
    </div>
    <div class="change_box">
      <button @click="change('tab_1')" :class="nowActive === 'tab_1' ? 'active' : ''">融资金额</button>
      <button @click="change('tab_2')" :class="nowActive === 'tab_2' ? 'active' : ''">融资成本</button>
    </div>
    <div class="chart_box"></div>
  </div>
</template>
<script>
export default {
  name: 'financingAmount',
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

.financing_amount {
  flex: 1;
}
</style>