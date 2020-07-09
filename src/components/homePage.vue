<template>
  <div class="home_page">
    <el-row :gutter="20" class="row-content">
      <div class="home-left">
        <el-col :span="8">
          <div class="money_collection">
            <div class="title">
              <dl>
                <dt><img src="../../static/images/triangle.png" alt=""></dt>
                <dd>资金归集分析</dd>
              </dl>
              <!-- <img src="../../static/images/zjclfx.png" alt=""> -->
            </div>
            <div class="echarts_box"></div>
          </div>
        </el-col>

        <!-- <el-col :span="8">
          <div class="money_collection">
            <div class="img_box">
              <img src="../../static/images/dejjtzfx.png" alt="">
            </div>
            <div class="echarts_box"></div>
          </div>
        </el-col>
        <el-col :span="8">
          <div class="money_collection">
            <div class="img_box">
              <img src="../../static/images/rzjejcbfx.png" alt="">
            </div>
            <div class="echarts_box"></div>
          </div>
        </el-col> -->
      </div>
      <!-- <div class="home-center">
        <el-col :span="8">
          <div class="money_collection">
            <div class="img_box">
              <img src="../../static/images/zjclfx.png" alt="">
            </div>
            <div class="echarts_box"></div>
          </div>
        </el-col>
        <el-col :span="8" :offset="8">
          <div class="money_collection">
            <div class="img_box">
              <img src="../../static/images/zjclfx.png" alt="">
            </div>
            <div class="echarts_box"></div>
          </div>
        </el-col>
      </div>
      <div class="home-right">
        <el-col :span="8">
          <div class="money_collection">
            <div class="img_box">
              <img src="../../static/images/zjclfx.png" alt="">
            </div>
            <div class="echarts_box"></div>
          </div>
        </el-col>
        <el-col :span="8">
          <div class="money_collection">
            <div class="img_box">
              <img src="../../static/images/zjclfx.png" alt="">
            </div>
            <div class="echarts_box"></div>
          </div>
        </el-col>
        <el-col :span="8">
          <div class="money_collection">
            <div class="img_box">
              <img src="../../static/images/zjclfx.png" alt="">
            </div>
            <div class="echarts_box"></div>
          </div>
        </el-col>
      </div> -->
    </el-row>
  </div>
</template>

<script>
export default {
  name: 'homePage',
  data () {
    return {
    
    }
  }
}
</script>
<style>
.home_page {
  width: 100%;
  height: 100%;
  position:fixed;
  top: 0;
  left: 0;
  background-image:url('../assets/images/bg.png');
  background-repeat: no-repeat;
  background-size: cover;
  z-index:-10;
  zoom: 1;
  background-position: center 0;
  overflow-y: auto;
}
.row-content {
  margin-top: 50px;
  display: flex;
  flex-direction: column;
}
.money_collection {
  dl {

  }
  
}
.img_box {
  width: 258px;
  height: 100px;
}
img {
  width: 100%;
  height: 100%;
}
.el-col .el-col-8 {
  text-align: left;
  
}
.echarts_box {
  width: 100%;
  height: 303px;
  border: 1px solid red;
  margin-left: 60px;
}
</style>
