<template>
  <div class="home_page">
    <div class="head_box">
      <dl class="left">
        <dt>
          <img src="../../static/images/icon.png" alt="">
        </dt>
        <dd>
          <span>融资规模</span>
          <span><em>388</em>亿元</span>
        </dd>
      </dl>
      <dl class="right">
        <dt>
          <img src="../../static/images/icon.png" alt="">
        </dt>
        <dd>
          <span>货币资金存量</span>
          <span><em>388</em>亿元</span>
        </dd>
      </dl>
    </div>
    <div class="home_content_box">
      <div class="left">
        <moneyCollection/>
        <largeInfrastructure/>
        <financingAmount/>
      </div>
      <div class="center">
        <launchMaps/>
        <capitalStock/>
      </div>
      <div class="right">
        <cashFlow/>
        <capitalPlan/>
      </div>
    </div>
  </div>
</template>
<script>
import moneyCollection from './moneyCollection'
import largeInfrastructure from './largeInfrastructure'
import financingAmount from './financingAmount'
import launchMaps from './launchMaps'
import capitalStock from './capitalStock'
import cashFlow from './cashFlow'
import capitalPlan from './capitalPlan'
export default {
  name: 'homePage',
  components: {
    moneyCollection, // 资金归集分析
    largeInfrastructure, // 大额基建投机分析
    financingAmount, // 融资金额及成本分析
    launchMaps, // 发射型地图
    capitalStock, // 资金存量分析
    cashFlow, // 现金流量分析
    capitalPlan,
  }
}
</script>
<style lang="scss">
@import '@/assets/css/rem.scss';

@keyframes rotate {
  from {
    transform: rotate(0deg);
  } to {
    transform: rotate(360deg);
  }
}
.home_page {
  width: 100%;
  height: 100%;
  position:fixed;
  top: 0;
  left: 0;
  z-index:-10;
  zoom: 1;
  overflow-y: auto;
  background-color: #020229;
  background-image: url("../assets/images/bg_01.png"), url("../assets/images/bg_02.png");
  background-repeat: no-repeat, no-repeat;  
  background-position: top center, bottom center; 
  background-size: 100% auto, 100% auto;
  > .head_box {
    position: fixed;
    left: 0;
    top: 0;
    width: 100%;
    height: rem(120px);
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: -rem(120px);
    align-items: flex-end;
    dl {
      width: rem(299px);
      height: rem(73px);
      background-image: url('../../static/images/bgleft.png');
      background-repeat: no-repeat;
      background-size: cover;
      background-position: center 0;
      z-index: -8;
      display: flex;
      justify-content: center;
      align-items: center;
      &.left {
        margin-left: rem(112px);
      }
      &.right {
        margin-right: rem(112px);
      }
      dt {
        line-height: 0px;
        img {
          width: rem(28px);
          height: rem(24px);
        }
      }
      dd {
        span {
          display: block;
          font-size: rem(15px);
          font-family: Source Han Sans CN;
          font-weight: bold;
          font-style: italic;
          color :#ffffff;
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
  > .home_content_box {
    display: flex;
    justify-content: space-between;
    height: 100%;
    box-sizing: border-box;
    padding-top: rem(120px);
    > div {
      flex: none;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      height: 100%;
      > div {
        width: 100%;
        display: flex;
        flex-direction: column;
        box-sizing: border-box;
        padding: rem(10px);
        position: relative;
        left: 0;
        top: 0;
        .title_box {
          position: relative;
          left: 0;
          top: 0;
          width: max-content;
          height: rem(150px);
          margin-top: rem(-50px);
          margin-bottom: rem(-40px);
          > .title {
            height: 100%;
          }
          > .ico {
            position: absolute;
            right: -rem(20px);
            bottom: rem(16px);
            height: rem(24rem);
            animation: rotate 1s linear infinite;
          }
        }
        .chart_box {
          flex: 1;
          border: 1px dashed #fff;
        }
        .change_box {
          position: absolute;
          right: 0;
          z-index: 2;
          top: rem(50px);
          display: flex;
          justify-content: center;
          align-items: center;
          > button {
            width:rem(89px);
            height:rem(28px);
            font-size:rem(15px);
            font-family:Microsoft YaHei;
            color:rgba(0,143,255,1);
            display: flex;
            align-items: center;
            justify-content: center;
            border:1px solid transparent;
            &.active {
              color: #ffffff;
              background:rgba(48,120,218,0.2);
              border:1px solid;
              border-image:linear-gradient(90deg, rgba(3,75,141,1), rgba(10,154,251,1), rgba(3,70,135,1)) 1 1;
              box-shadow:0px 0px 38px 0px rgba(5,47,112,0.86);
            }
          }
        }
      }
      &.left {
        width: 30%;
      }
      &.center {
        width: 40%;
      }
      &.right {
        width: 30%;
      }
    }
  }
}
</style>