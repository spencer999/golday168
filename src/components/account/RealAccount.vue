<template> 	
	<section class="register">
	<h3>欢迎开立真实账户</h3>
    <form id="form" action="/Login/tgregister.html" method="post" class="form-horizontal" onsubmit="return false;">

      <div class="js_inputBox">
        <div class="line">
          <span>真实姓名</span>
          <input type="text" class="name" name="name" placeholder="与身份证一致" onclick="ga ('send','event','m_lp_open_account','name','content_first')">
        </div>
        <p class="tip js_tipN"></p>
        <div class="line">
          <span>身份证号</span>
          <input type="text" class="cordno" name="cordno" placeholder="请填写居民身份证号码" onclick="ga ('send','event','m_lp_open_account','identity','content_first')">
        </div>
        <p class="tip js_tipID"></p>
        <div class="line">
          <span>手机号码</span>
          <input type="text" class="mobile" name="mobile" placeholder="请输入银行预留手机号码" onclick="ga ('send','event','m_lp_open_account','cell phone','content_first')">
        </div>
        <p class="tip js_tipM"></p>
        <div class="line">
          <span>电子邮箱</span>
          <input type="text" class="email" name="email" placeholder="接收账户重要信息" autocomplete="off" onclick="ga ('send','event','m_lp_open_account','mail','content_first')">
          <ul class="dataul">
            <li><i class="same"></i>@qq.com </li>
            <li><i class="same"></i>@gmail.com</li>
            <li><i class="same"></i>@126.com</li>
            <li><i class="same"></i>@163.com</li>
            <li><i class="same"></i>@hotmail.com</li>
            <li><i class="same"></i>@yahoo.com</li>
          </ul>
        </div>
        <p class="tip js_tipY"></p>

        <div class="line">
          <span>图片验证</span>
          <input type="text" class="w35 imgVerify" name="imgVerify" placeholder="请输入图片验证码" onclick="ga ('send','event','m_lp_open_account','auth code','content_first')">
          <img class="w16 verifyimg js_verifyImg" src="/Login/verifyImg.html" width="130">
        </div>
        <p class="tip js_tipV"></p>

        <div class="line">
          <span>短信验证</span>
          <input type="text" class="w35 verifyCode" name="verify" placeholder="请输入手机验证码">
          <div class="w16 js_getCode" onclick="getSMS();ga ('send','event','m_lp_open_account','testgetcode','conten_first');">
            获取验证码 </div>
        </div>
        <p class="tip js_tipC"></p>
        <p class="contact">若长时间未取到验证码，请联系<span class="orange js_kefu" onclick="ga ('send','event','m_lp_open_account','chat_live800','conten_first');">在线客服</span>索取
          &nbsp;&nbsp;&nbsp;</p>

       
        <div class="registerBtn" id="sumbit" onclick="ga ('send','event','m_lp_open_account','register','content_first');">确认注册</div>
        <p class="contact tc"><!-- <img src="__PUBLIC__/images/mobile/message.png">  -->离领取<span class="orange">10000美元</span>还差一步</p>
        <p class="remember">已有账户，点击<a class="red" href="{:U('Index/login')}"> 登录</a></p>
      </div>
       <div class="tc">
          <span class="check"> ✔ </span>
          <span class="remember">我已仔细阅读并同意 <a href="http://m.golday.com/Mobile/Index/contract.html"> 《金盛贵金属客户协议》</a></span>
        </div>
    </form>
    <!-- </div>  -->
    <div class="none"></div>
    <div class="loading js_loading">
     <!--  <img src="__PUBLIC__/images/mobile/loading.gif"> -->
    </div>
  </section>
</template>

<script>
export default {
   	name: 'foot',
   	data () {
	    return {
	        msg: '金盛贵金属官网_正规香港贵金属交易平台', 
	    }
    }
}
</script>
 
<style>
	.register {
      width: 7rem;
      margin: .25rem auto;
      background: #fff;
      padding: .3rem .2rem .5rem;
    }
	.register h3{
		text-align: center;
		font-size:.3rem;
		color:#333;

	}
    .register label {
      margin-bottom: 0;
      font-weight: 500;
    }
 
 
    .register .line {
      width: 6.6rem;
      height: .78rem;
      line-height: .78rem;
      margin: .3rem auto 0rem;
      border-radius: 5px;
     /*  border: 1px solid #ddd; */
      position: relative;
      font-size:0;
    }

    .register .line.redBorder {
      border: 1px solid #ff5555;
    }

    .register .line span {
      width: 1.6rem;
      height: 100%;
      text-align: center;
      font-size: .26rem;
      color: #333;
      line-height: .78rem;
      vertical-align: top;
     /*  border-right: 1px solid #d1d1d1; */
    }

    .register .line input {
      width: 4.5rem;
      border: 1px solid #ddd;
      line-height: .78rem;
      border-radius:3px;
      font-size: .26rem;
      padding-left: .3rem;
      display: inline-block;
      vertical-align: top;
    }

    .register .line .w35 {
        width: 2.7rem;
    	margin-right: .2rem;
    }

    .register .line .w16 {
	    display: inline-block;
	    width: 1.6rem;
	    background: #fcaa2c;
	    color: #fff;
	    text-align: center;
	    font-size: .26rem;
	    border-radius: 3px;
	    height: 100%;
	    vertical-align: top;
    }

    .register .contact {
      text-align: right;
      font-size: .24rem;
      color: #666;
      line-height: .6rem;
      margin-bottom: .15rem;
    }

    .register .contact img {
      width: .26rem;
      height: .21rem;
      vertical-align: center;
    }

    .register .registerBtn {
      width: 100%;
      height: .82rem;
      line-height: .82rem;
      text-align: center;
      background: #fcaa2c;
      color: #fff;
      font-size: .36rem;
      margin: .2rem auto 0;
      border-radius: 5px;
      border: none;
    }

    .register .orange {
      color: #fcaa2c;
    }

    .register .check {
      width: .25rem;
      height: .25rem;
      font-size: .2rem;
      line-height: .25rem;
      margin-top: 0.05rem;
      text-align: center;
      background: #fff;
      border: 1px solid #d1d1d1;
      border-radius: 3px;
      vertical-align: middle;
    }

    .register .remember {
      font-size: .24rem;
      color: #333;
      margin-left: .2rem;
      vertical-align: middle;
      text-align: center;
    }

    .register .loading {
      display: none;
      width: 100%;
      height: 100%;
      position: fixed;
      top: 0;
      left: 0;
      padding-top: 65%;
      z-index: 100
    }

    .register .loading img {
      width: 2.30rem;
      height: 2.30rem;
      display: block;
      margin: 0 auto;
    }
	.register .red {
      color: #ff5555;
    }

    .register .tc {
      text-align: center !important;
    }

    .register .tip {
      line-height: .4rem;
      color: #ff5555;
      margin: .05rem 0 0 1.7rem;
      font-size: .24rem;
    }

    .register .dataul {
      display: none;
      border: 1px solid #aaa;
      box-sizing: border-box;
      padding: .25rem;
      margin-left: 1.6rem;
      list-style: none;
      background: #fff;
      position: absolute;
      left: 0;
      top: .8rem;
      z-index: 100;
    }

    .register .dataul li {
      line-height: 1.2;
      font-size: .26rem;
    }

    .register .dataul li i {
      font-style: normal;
      line-height: 1.7;
    }
</style>
 