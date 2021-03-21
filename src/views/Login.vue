<template>
    <div class="home">
        <!-- 上边黄框 开始-->
        <div class="head-container">

            <!-- 标题+logo 开始-->
            <div class="left">
                <div>
                    <img src="../assets/Home/logo3.png" alt="" style="height:70px;width:70px;margin-right:10px;margin-left:20px;">
                </div>
                <div>
                     <h1 style="font-family:'PingFang SC';
                        font-weight:bold;
                        color:#1C3263;
                        font-size:130%;
                        margin-left: 5px;">共享租赁平台</h1>
                </div>
            </div>
            <!-- 标题+logo 结束-->

            <!-- 中间框 开始-->
            <div class="middle">
                <!-- 搜索栏 -->
                <div style="width:80%;" class="search">
                    <form action="#" method="post">
                        <img src="../assets/Home/搜索图标.png" alt="">
                        <input type="text" name="condition" placeholder="">
                    </form>	
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
            </div>
            <!-- 中间框 结束-->

            <!-- 头像 + 登录/注册 + 购物车图标 + 收藏图标 开始-->
            <div class="right">
                <img src="../assets/Home/图片@1x.png" alt="" style="width:60px;height:60px;margin-right:20px;">
                <span style="font-weight:bold;">登录/注册</span>
                <img src="../assets/Home/shopping-cart.png" alt="" style="height:30px; width:30px; margin-left:20px;">
                <img src="../assets/Home/like.png" alt="" style="height:30px; width:30px; margin-left:16px;">
            </div>
            <!-- 头像 + 登录/注册 + 购物车图标 + 收藏图标 结束-->

        </div>
        <!-- 上边黄框 结束-->

        <!-- 中部登录/注册部分，开始 -->
        <div class="main-content" style="width: 80%; height: 450px; margin: 30px auto;">
            <!-- 左部注册部分，开始 -->
            <div class="register" style="width: 59%; height: 449px; 
                                         border-style: none none outset outset; 
                                         border-color: rgba(169, 169, 169, 0.637);
                                         border-top-left-radius: 20px;border-bottom-left-radius: 20px;
                                         ">

                <!-- 顶部提示 -->
                <div style="font-size: 140%; width: 60%;
                            padding-top: 40px; margin: 0 auto;
                            flex-direction: row; justify-content: space-between;
                            font-weight:bold; align-items: center;
                            text-align: center;">新用户？在此注册</div>
                <!-- 顶部提示语，结束 -->

                <!-- 中部输入表单，开始 -->
                <div>
                    <form >
                        <div class="inputs">
                            <a>*</a>
                            <span style="margin-right: 25px;;">姓名</span>
                            <input type="text" name="sex" id="name" placeholder="name" />
                            <span style="margin-left: 5px; font-family: monospace;">请勿输入特殊字符</span>
                        </div>                      
                        <div class="inputs">
                            <a>*</a>
                            <span style="margin-right: 25px;">昵称</span>
                            <input type="text" name="sex" id="nickname" placeholder="nickname" />
                            <span style="margin-left: 5px; font-family: monospace;">请勿输入特殊字符</span>
                        </div>
                        <div class="inputs">
                            <a>*</a>
                            <span style="margin-right: 25px;">密码</span>
                            <input type="password" name="sex" id="password" placeholder="password" />
                            <span style="margin-left: 5px; font-family: monospace;">请勿输入特殊字符</span>
                        </div>
                        <div class="inputs">
                            <a>*</a>
                            <span style="margin-right: 25px;">邮箱</span>
                            <input type="text" name="sex" id="email" placeholder="email" />
                            <button style="margin-left: 10px; height: 25px; text-align: center;">点击发送</button> 
                            <span style="margin-left: 5px; font-family: monospace;">接收确认邮件验证邮箱</span>
                        </div>
                        <div class="inputs">
                            <a>*</a>
                            <span style="margin-right: 10px;">手机号</span>
                            <input type="text" name="sex" id="phone-number" placeholder="phone number" />
                            <button style="margin-left: 10px; height: 25px; text-align: center;">点击发送</button>
                            <span style="margin-left: 5px; font-family: monospace;">接收确认短信验证手机号</span>
                        </div>
                        <div class="inputs">
                            <a>*</a>
                            <span style="margin-right: 10px;">验证码</span>
                            <input type="text" name="sex" id="code" placeholder="code" />
                            <span style="margin-left: 5px; font-family: monospace;">输入四位验证码</span>
                        </div>
                        <div class="inputs">
                            <a>*</a>
                            <b style="font-family: monospace;">使用此网站即代表您同意条款和条件</b>
                        </div>
                    </form>
                </div>
                <!-- 中部输入表单，结束 -->

                <!-- 底部注册按钮，开始 -->
                <div style="width: 80%; height: 30px; margin: 10px 25px;">
                    <button style=" width: 100%; 
                                   height: 100%; 
                                   text-align: center; 
                                   background-color: #F2B50F;
                                   border-radius: 5px;
                                   border: none;
                                   outline: none;">注册</button>
                </div>
                <!-- 底部注册按钮，结束 -->
            </div>
            <!-- 左部注册部分，结束 -->

            <!-- 右部登录部分，开始 -->
            <div class="log" style="width: 40%; height: 449px; background-color: rgba(208, 211, 212, 0.692);
                                    border-style: none outset outset none; 
                                         border-color: rgba(169, 169, 169, 0.637);
                                         border-top-right-radius: 20px;
                                         border-bottom-right-radius: 20px;">
                <!-- 顶部提示语，开始 -->
                <div style="font-size: 140%;width: 60%;padding-top: 40px;
                            margin: 0 auto;flex-direction: row;justify-content: space-between;
                            font-weight:bold;align-items: center;
                            text-align: center;">已有账号？在此登录</div>
                <!-- 顶部提示语，结束 -->

                <!-- 账号密码登录，开始 -->
                <div>
                    <div class="in">
                        <a>*</a>
                        <span style="margin-right: 10px;">用户名/账号/手机号</span>
                        <input type="text" name="sex" id="account" placeholder="aaa@qq.com" />
                    </div>
                    <div class="in">
                        <a>*</a>
                        <span style="margin-right: 66px;">密码/验证码</span>
                        <input type="password" name="sex" id="verify" placeholder="******" />
                    </div>

                    <!-- 中部登录按钮，开始 -->
                    <div style="width: 80%; height: 30px; margin: 40px auto;">
                        <button style=" width: 100%;  height: 100%; 
                                    text-align: center;  background-color: #2629b8b6;
                                    border-radius: 5px; border: none; color: seashell;
                                    outline: none;">登录</button>
                    </div>
                    <!-- 中部登录按钮，结束 -->

                </div>
                <!-- 账号密码登录，结束 -->

                <!-- 其它登录方式，开始 -->
                <div class="others" style="width: 100%; ">
                    <!-- 分割线 -->
                    <div style="font-family: monospace;  font-weight: bolder; 
                                 margin-top: 60px; text-align: center;">
                            —————————其它登录方式—————————
                    </div>

                    <!-- 其它方式图标 -->
                    <div class="icons">
                        <a href="#">
                            <img src="../assets/Home/qq.png" alt="">
                        </a>
                        <a href="#">
                            <img src="../assets/Home/微信.png" alt="">
                        </a>
                        <a href="#">
                            <img src="../assets/Home/支付宝.png" alt="">
                        </a>
                    </div>
                </div>
                <!-- 其它登录方式，结束 -->

            </div>
            <!-- 右部登录部分，结束 -->

        </div>
        <!-- 中部登录/注册部分，结束 -->
        
    </div>
    <!-- 整体结束 -->
</template>

<script>
import { defineComponent } from '@vue/composition-api'

export default defineComponent({
    setup() {
        
    },
})
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
        
        .head-container .left{
          width: 20%;
          direction: horizontal;
          display: flex;
          justify-content: center;
          align-items: center;
        }
        
        .head-container .middle{
          /* background-color: #8f8d85; */
          width: 48%;
          direction: vertical;
          display: flex;
          flex-direction: column;
          justify-content: center;
          align-items: center;
        }
        
        .search .form{
            height: 100%;
            width: 100%;
            /* color: #1C3263; */
        }

        .search form input:nth-child(2){
			width: 470px;
			height: 30px;
			font-size: 16px;
			text-indent: 45px;
			border: none;
			float: left;
            border-radius: 15px;
            outline: none;
		}

        .search form img{
			position: absolute;
			left: 50vw;
			transform: translateX(-250px);
			margin-top: 10px;
			margin-left: 5px;
            height: 15px;
		}

        .head-container .right{
          width: 23%;
          direction: horizontal;
          display: flex;
          justify-content: center;
          align-items: center;
        }

        form div{
            margin-top: 20px;
            margin-left: 30px;
        }

        .inputs a{
           color: rgb(197, 21, 21);
        }

        .inputs input{
            height: 20px;
            outline: none;
        }

        .register, .log{
            float: left;
        }

        .in{
            margin: 20px;
        }
        .in a{
           color: rgb(197, 21, 21);
        }
        .in input{
            height: 20px;
            outline: none;
        }

        .icons img{
            height: 90px;
            margin-top: 20px;
            margin-left: 25px;
        }
</style>
