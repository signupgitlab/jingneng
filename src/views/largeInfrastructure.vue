<template>
  <div class="large_infrastructure">
    <div class="title_box">
      <img class="title" src="../../static/images/dejjtzfx.png" alt="">
      <img class="ico" src="../../static/images/ae.png" alt="">
    </div>
    <div class="some_con">
      <div class="chart_box"></div>
      <div class="other">
        <div class="tip_list">
          <div>
            <span style="background: #0090FF;"></span>
            <p>本年计划投资额</p>
          </div>
          <div>
            <span style="background: #07C9C2;"></span>
            <p>本年累计支付资金</p>
          </div>
        </div>
        <div class="tip_card">
          <div>本年计划投资额</div>
          <span><em>394</em>亿元</span>
        </div>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
@import '@/assets/css/rem.scss';

.large_infrastructure {
  flex: 1;
  .some_con {
    display: flex;
    justify-content: space-between;
    height: 100%;
    .other {
      height: 100%;
      .tip_list {
        display: flex;
        flex-direction: column;
        justify-content: center;
        padding-left: rem(10px);
        margin-bottom: rem(10px);
        > div {
          display: flex;
          align-items: center;
          & + div {
            margin-top: rem(15px);
          }
          > span {
            display: block;
            width: rem(10px); 
            height: rem(10px); 
          }
          p {
            margin-left: rem(10px);
            font-size:rem(15px);
            font-family:Microsoft YaHei;
            color:rgba(145,189,235,1);
          }
        }
      }
      .tip_card {
        width:rem(156px);
        height:rem(128px);
        background:rgba(255,255,255,0);
        border:1px solid;
        border-image:linear-gradient(90deg, rgba(3,75,141,1), rgba(10,154,251,1), rgba(3,70,135,1)) 1 1;
        box-shadow:0px 0px 38px 0px rgba(5,47,112,0.86);
        display: flex;
        justify-content: center;
        align-items: flex-start;
        flex-direction: column;
        > div {
          font-size:rem(15px);
          font-family:Microsoft YaHei;
          color:rgba(255,255,255,1);
          margin-left: rem(20px);
        }
        span {
          display: block;
          font-size: rem(15px);
          font-family: Source Han Sans CN;
          font-weight: bold;
          font-style: italic;
          color :#ffffff;
          margin-top: rem(18px);
          margin-left: rem(20px);
        }
        em {
          font-size: rem(24px);
          font-family: Enter Sansman;
          font-weight: bold;
          font-style: italic;
        }
      }
    }
  }
}
</style>