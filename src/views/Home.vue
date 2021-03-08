<template>
  <div class="home">
    <!-- 上边黄框 开始-->
    <el-container class="head-container">

      <!-- 标题+logo 开始-->
      <el-container class="left">
        <img src="../assets/Home/logo3.png" alt="" style="height:70px;width:70px;margin-right:20px;margin-left:20px;">
        <h1 style="font-family:'PingFang SC';
                  font-weight:bold;
                  color:#1C3263;
                  font-size:130%;">共享租赁平台</h1>
      </el-container>
      <!-- 标题+logo 结束-->

      <!-- 中间框 开始-->
      <el-container class="middle">
        <!-- 搜索栏 -->
        <div style="width:80%;">
          <el-input placeholder="请输入内容"
                    prefix-icon="el-icon-search"
                    v-model="input1">
          </el-input>
        </div>
        <!-- 热门搜索建议 -->
        <div style="width: 80%;
                  margin-top: 8px;
                  display: flex;
                  flex-direction: row;
                  justify-content: space-between;
                  font-size:12px;
                  font-weight:bold;
                  align-items: center;">
          <span>小皮鞋</span>
          <span>三角钢琴</span>
          <span>女士礼服</span>
          <span>高定礼服</span>
          <span>珍珠项链</span>
          <span>西装外套</span>
          <span>更多...</span>
        </div>
      </el-container>
      <!-- 中间框 结束-->

      <!-- 头像 + 登录/注册 + 购物车图标 + 收藏图标 开始-->
      <el-container class="right">
        <img src="../assets/Home/图片@1x.png" alt="" style="width:60px;height:60px;margin-right:20px;">
        <span style="font-weight:bold;">登录/注册</span>
        <img src="../assets/Home/shopping-cart.png" alt="" style="height:30px; width:30px; margin-left:20px;">
        <img src="../assets/Home/like.png" alt="" style="height:30px; width:30px; margin-left:16px;">
      </el-container>
      <!-- 头像 + 登录/注册 + 购物车图标 + 收藏图标 结束-->

    </el-container>
    <!-- 上边黄框 结束-->

    <!-- 轮播图 -->
    <el-carousel indicator-position="none">
      <el-carousel-item v-for="index in 4" :key="index">
        <img src="../assets/Home/轮播1.png" v-if="index % 2 == 0" class="bannerImg" />
        <img src="../assets/Home/轮播2.png" v-if="index % 2 == 1" class="bannerImg" />
      </el-carousel-item>
    </el-carousel>

    <!-- 下面大框 开始-->
    <el-container class="bottom">

      <el-container :class="categoryContainerActive? 'left':'leftHidden'">

        <el-container class="constrained" @click.native="changeCategoryShow ()">
          <span>产</span>
          <span>品</span>
          <span>分</span>
          <span>类</span>
        </el-container>
        <!-- 具体分类 开始-->
        <el-container :class="categoryContainerActive? 'stretched':'stretchedHidden'">
          <el-container @click.native="changeItemActive (0)" :class="(categoryContainerActive && categoryItemActive[0])? 'alineActive':'aline'">
            <img src="../assets/Home/包.png" style="height:23px;width:23px;margin-right:10px;"/>
            <span>鞋品 / 箱包</span>
            <span>＞</span>
          </el-container>

          <el-container :class="(categoryContainerActive && categoryItemActive[1])? 'alineActive':'aline'" @click.native="changeItemActive(1)">
            <img src="../assets/Home/饰品.png" style="height:23px;width:23px;margin-right:10px;"/>
            <span>饰品 / 配件</span>
            <span>＞</span>
          </el-container>

          <el-container :class="(categoryContainerActive && categoryItemActive[2])? 'alineActive':'aline'" @click.native="changeItemActive(2)">
            <img src="../assets/Home/家具.png" style="height:23px;width:23px;margin-right:10px;margin-top:2px;"/>
            <span>家具 / 家电</span>
            <span>＞</span>
          </el-container>

          <el-container :class="(categoryContainerActive && categoryItemActive[3])? 'alineActive':'aline'" @click.native="changeItemActive(3)">
            <img src="../assets/Home/乐器.png" style="height:23px;width:23px;margin-right:10px;"/>
            <span>乐器 / 设备</span>
            <span>＞</span>
          </el-container>

          <el-container :class="(categoryContainerActive && categoryItemActive[4])? 'alineActive':'aline'" @click.native="changeItemActive(4)">
            <img src="../assets/Home/book.png" style="height:23px;width:23px;margin-right:10px;"/>
            <span>书籍 / 学习</span>
            <span>＞</span>
          </el-container>

          <el-container :class="(categoryContainerActive && categoryItemActive[5])? 'alineActive':'aline'" @click.native="changeItemActive(5)">
            <img src="../assets/Home/机械.png" style="height:23px;width:23px;margin-right:10px;"/>
            <span>机械 / 重器</span>
            <span>＞</span>
          </el-container>

          <el-container :class="(categoryContainerActive && categoryItemActive[6])? 'alineActive':'aline'" @click.native="changeItemActive(6)">
            <img src="../assets/Home/旅行装备.png" style="height:23px;width:23px;margin-right:10px;"/>
            <span>旅行 / 装备</span>
            <span>＞</span>
          </el-container>

          <el-container :class="(categoryContainerActive && categoryItemActive[7])? 'alineActive':'aline'" @click.native="changeItemActive(7)">
            <img src="../assets/Home/礼服.png" style="height:23px;width:23px;margin-right:10px;"/>
            <span>礼服 / 戏服</span>
            <span>＞</span>
          </el-container>
        </el-container>
        <!-- 具体分类 结束-->

      </el-container>

      <!-- 猜你喜欢大框 开始-->
      <el-container class="right">

        <!-- 猜你喜欢标题 -->
        <el-container class="guessYouLike-title-container">
          <span style="font-weight:bold;color: #1C3263;">猜你喜欢</span>
          <div class="a-short-line"></div>
        </el-container>

        <!-- 猜你喜欢内容1 开始-->
        <el-container style="guessYouLike-content-aline-container">
          <el-col :span="4" v-for="(o, index) in 5" :key="o" :index="index" :offset="index > 0 ? 1:0">
            <el-card :body-style="{ padding: '0px' }">
              <img src="../assets/Home/item1.png" v-if="index == 0" class="image">
              <img src="../assets/Home/item2.png" v-if="index == 1" class="image">
              <img src="../assets/Home/item3.png" v-if="index == 2" class="image">
              <img src="../assets/Home/item4.png" v-if="index == 3" class="image">
              <img src="../assets/Home/item5.png" v-if="index == 4" class="image">
              <div class="guessYouLike-content-cell">
                <span>{{itemNameArray1[index]}}</span>
              </div>
              <div class="guessYouLike-content-cell">
                <span>RMB {{itemPriceArray1[index]}} /天</span>
              </div>
            </el-card>
          </el-col>
        </el-container>
        <!-- 猜你喜欢内容1 结束-->

        <!-- 行中间占位框 -->
        <div style="height:30px;width:100%;"></div>

        <!-- 猜你喜欢内容2 开始-->
        <el-container style="guessYouLike-content-aline-container">
          <el-col :span="4" v-for="(o, index) in 5" :key="o" :index="index" :offset="index > 0 ? 1:0">
            <el-card :body-style="{ padding: '0px' }">
              <img src="../assets/Home/item1.png" v-if="index == 0" class="image">
              <img src="../assets/Home/item2.png" v-if="index == 1" class="image">
              <img src="../assets/Home/item3.png" v-if="index == 2" class="image">
              <img src="../assets/Home/item4.png" v-if="index == 3" class="image">
              <img src="../assets/Home/item5.png" v-if="index == 4" class="image">
              <div class="guessYouLike-content-cell">
                <span>{{itemNameArray2[index]}}</span>
              </div>
              <div class="guessYouLike-content-cell">
                <span>RMB {{itemPriceArray2[index]}} /天</span>
              </div>
            </el-card>
          </el-col>
        </el-container>
        <!-- 猜你喜欢内容2 结束-->
      </el-container>
      <!-- 猜你喜欢大框 开始-->

    </el-container>
    <!-- 下面大框 结束-->

    <!-- 最下方占位框 -->
    <div style="height:30px;"></div>
  </div>
</template>

<script>
// @ is an alias to /src
export default {
  name: 'home',
  data () {
    return {
      input1: '',
      itemNameArray1: ['测试名牌运动鞋001', '测试名牌连衣裙001', '测试名牌运动鞋002', '测试名牌戒指001', '测试名牌帽子001'],
      itemPriceArray1: ['10.00', '20.00', '30.00', '40.00', '50.00'],
      itemNameArray2: ['测试名牌运动鞋001', '测试名牌连衣裙001', '测试名牌运动鞋002', '测试名牌戒指001', '测试名牌帽子001'],
      itemPriceArray2: ['10.00', '20.00', '30.00', '40.00', '50.00'],
      categoryContainerActive: false,
      categoryItemActive: [true, false, false, false, false, false, false, false]
    }
  },
  methods: {
    changeCategoryShow () {
      this.categoryContainerActive = !this.categoryContainerActive
      console.log(this.categoryContainerActive)
    },
    changeItemActive (i) {
      for (var j = 0; j < this.categoryItemActive.length; i++) {
        this.categoryItemActive[j] = false
      }
      this.categoryItemActive[i] = true
      console.log(this.categoryItemActive)
    }
  }
}
</script>

<style scoped>
.head-container{
  background-color: #F2B50F;
  width: 100%;
  height: 90px;
  direction: horizontal;
  display: flex;
  justify-content: space-between;
}

.head-container.left{
  width: 20%;
  direction: horizontal;
  display: flex;
  justify-content: center;
  align-items: center;
}

.head-container .middle{
  /*background-color: #8f8d85;*/
  width: 48%;
  direction: vertical;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.head-container .right{
  width: 23%;
  direction: horizontal;
  display: flex;
  justify-content: center;
  align-items: center;
}
.lunbo-container{
  width: 100%;
  height: 300px;
  background-color: aliceblue;
  display: flex;
  align-content: stretch;
}
.bannerImg{
  width: 100%;
  height: 300;
}
.guessYouLike-title-container{
  width: 95%;
  height: 100px;
  justify-content: center;
  align-items: center;
  display: flex;
  flex-direction: column;
}
.guessYouLike-title-container .a-short-line{
  width: 70px;
  height: 3px;
  background-color: #FFD768;
  margin-top: 2px;
}
.guessYouLike-content-container{
  width: 80%;
  height: 200px;
  justify-content: center;
  align-items: flex-start;
  display: flex;
  flex-direction: column;
}
.guessYouLike-content-aline-container{
  height: 80px;
  justify-content: center;
  align-items: center;
}
.guessYouLike-content-cell{
  width: 100%;
  justify-content: flex-start;
  align-items: center;
  text-align: left;
  margin-top: 10px;
  margin-left: 10px;
  margin-bottom: 10px;
}
.bottom {
  width: 100%;
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: flex-start;
}
.bottom .left{
  width: 15%;
  height:500px;
  margin-top: 60px;
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: flex-start;
  border-top-right-radius: 10px;
  border-bottom-right-radius: 10px;
  background-color: #FFD768;
  box-shadow: 1px 0.3px 5px rgb(182, 181, 181);
}
.bottom .leftHidden{
  width: 15%;
  height:500px;
  margin-top: 60px;
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: flex-start;
}
.constrained{
  width: 20px;
  height: 500px;
  background-color: #FFD768;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border-top-right-radius: 10px;
  border-bottom-right-radius: 10px;
  box-shadow: 1px 0.3px 5px rgb(182, 181, 181);
}
.stretched{
  height:500px;
  width: 170px;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.stretchedHidden{
  height:500px;
  width: 170px;
  display: flex;
  flex-direction: column;
  align-items: center;
  opacity: 0;
}
.stretched .aline{
  display: flex;
  width: 95%;
  flex-direction: row;
  justify-content: space-evenly;
  align-items: center;
  margin-top: 14px;
  margin-bottom: 14px;
}
.stretched .alineActive{
  display: flex;
  width: 95%;
  flex-direction: row;
  justify-content: space-evenly;
  align-items: center;
  background-color: rgb(255, 255, 255);
  border-radius: 20px;
  border-width: 1px;
  border-color: rgb(177, 177, 182);
  border-style: solid;
  margin-top: 14px;
  margin-bottom: 14px;
}
.bottom .right{
  width: 85%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-left: 20px;
}
.image {
  width: 100%;
  display: block;
}

body > .el-container {
  margin-bottom: 40px;
}

.el-container:nth-child(5) .el-aside,
.el-container:nth-child(6) .el-aside {
  line-height: 260px;
}

.el-container:nth-child(7) .el-aside {
  line-height: 320px;
}
</style>
