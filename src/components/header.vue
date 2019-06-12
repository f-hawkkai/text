<template>
    <div class="head">
         <div class="tou">
      <ul class="tu">
        <li class="oli ali">
          <img src="../assets/img/tou.jpg" width="220" height="50px">
        </li>
        <li class="oli">
          <img src="../assets/img/tou1.jpg">
        </li>
        <li class="ol">
          <h3 class="zi lg">成长守护平台</h3>
          <h3 class="zi">腾讯游戏排行榜</h3>
        </li>
      </ul>
    </div>
    <div class="header">
      <!--一级导航-->
      <div class="header-inner">
        <div class="log">
          <img src="../assets/img/alogo.png">
        </div>
        <ul class="let">
          <li>
            <a href="#">
              官网首页
              <em>home</em>
            </a>
          </li>
          <li>
            <a href="#">
              游戏资料
              <em>data</em>
            </a>
          </li>
          <li>
            <a href="#">
              内容中心
              <em>contents</em>
            </a>
          </li>
          <li>
            <a href="#">
              赛事中心
              <em>match</em>
            </a>
          </li>
          <li>
            <a href="#">
              百态王者
              <em>culture</em>
            </a>
          </li>
          <li>
            <a href="#">
              社区互动
              <em>community</em>
            </a>
          </li>
          <li>
            <a href="#">
              玩家支持
              <em>player</em>
            </a>
          </li>
        </ul>
        <div class="login">
          <span>
            <a href="#">
              <img src="../assets/img/login.png">
            </a>
          </span>
          <div class="log_in">
            <a href="#">欢迎登陆</a>
            <p>登录后查看游戏战绩</p>
          </div>
        </div>
      </div>
      <!-- 二级导航 -->
      <div class="header_two">
        <ul>
          <li>&nbsp;</li>
          <li>
            <a href="#">版本介绍</a>
            <a href="#">游戏介绍</a>
            <a href="#">英雄资料</a>
            <a href="#">爆料站</a>
            <a href="#">故事站</a>
            <a href="#">游戏壁纸</a>
          </li>
          <li>
            <a href="#">攻略中心</a>
            <a href="#">英雄攻略</a>
            <a href="#">视频中心</a>
            <a href="#">王者视角</a>
            <a href="#">作者入驻</a>
            <a href="#">媒体入驻</a>
          </li>
          <li>
            <a href="#">KPL</a>
            <a href="#">KPKPL</a>
            <a href="#">冠军杯</a>
            <a href="#">高校赛</a>
            <a href="#">城市赛</a>
            <a href="#">全民赛</a>
            <a href="#">赛事数据</a>
          </li>
          <li>
            <a href="#">荣耀·传承</a>
            <a href="#">王者文化站</a>
            <a href="#">王者音乐所</a>
            <a href="#">万千世界</a>
            <a href="#">星光殿堂</a>
            <a href="#">WiFi特权</a>
          </li>
          <li>
            <a href="#">王者营地</a>
            <a href="#">手Q部落</a>
            <a href="#">微信圈子</a>
            <a href="#">官方微博</a>
            <a href="#">微信公众号</a>
            <a href="#">手Q订阅号</a>
            <a href="#">同仁社区</a>
          </li>
          <li>
            <a href="#">成长守护平台</a>
            <a href="#">健康系统</a>
            <a href="#">狄仁杰护卫站</a>
            <a href="#">客服专区</a>
            <a href="#">礼包兑换</a>
            <a href="#">自助服务</a>
          </li>
        </ul>
      </div>
    </div>
    </div>
</template>
<script>
export default {
    
}
</script>
<style scoped>
* {
  margin: 0;
  padding: 0;
}
li {
  list-style: none;
}
em {
  font-style: normal;
}
body {
  padding-top: 42px;
  overflow-x: hidden;
}
a {
  text-decoration: none;
  color: #c9c9dd;
}
.tou {
  width: 100%;
  border-width: 1px 0;
  position: absolute;
  height: 42px;
  left: 0;
  top: 0 !important;
  border: 1px solid #c9c9c9;
}
.tou .tu {
  width: 950px;
  margin: 0 auto;
}
.oli {
  float: left;
}
.ali {
  width: 205px;
  padding: 0 15px 0 0;
  background-position: 0 -40px;
  position: relative;
  z-index: 10001;
}
.ol {
  float: right;
}
.zi {
  float: left;
  width: 118px;
  font-size: 12px;
  font-weight: 400;
  cursor: pointer;
  text-indent: 2rem;
  line-height: 40px;
}
.lg {
  background: url(../assets/img/logo.png) 12px no-repeat;
}
.header {
  width: 100%;
  position: absolute;
  top: 42px;
  left: 0;
  height: 85px;
  background: rgba(0, 0, 0, 0.8);
}
.header:hover .header_two {
  height: 240px;
}
.log {
  float: left;
}
.log img {
  position: absolute;
  top: 16px;
  left: 0;
}
.header-inner {
  width: 1200px;
  height: 84px;
  position: relative;
  margin: 0 auto;
}
.let {
  width: 790px;
  float: left;
  padding-left: 230px;
}
.let li {
  width: 110px;
  float: left;
  height: 84px;
  text-align: center;
  box-sizing: border-box;
}
.let li:hover {
  border-bottom: 3px solid #e4b653;
}
.let li:hover a {
  color: #e4b653;
}
.let li:hover a em {
  color: #e4b653;
}
.let li a {
  display: block;
  width: 110px;
  height: 64px;
  line-height: 30px;
  color: #c9c9dd;
  font-size: 18px;
  padding: 20px 0 0;
}
.let li a em {
  display: block;
  padding-top: 5px;
  font-size: 12px;
  line-height: 16px;
  color: #858792;
  text-transform: uppercase;
}
.login {
  width: 182px;
  position: absolute;
  right: 0;
  top: 21px;
}
.login img {
  border: 1px solid #d9ad50;
  border-radius: 42px;
}
.login span {
  display: block;
  float: left;
}
.login .log_in {
  float: left;
  width: 130px;
  margin-left: 5px;
}
.log_in a {
  color: #fff;
}
.log_in p {
  font-size: 14px;
  color: #858792;
  padding-top: 3px;
}
.header_two {
  width: 100%;
  position: absolute;
  top: 86px;
  left: 0;
  background: rgba(0, 0, 0, 0.7);
  transition: all 0.3s ease;
  z-index: 3;
  height: 0;
  overflow: hidden;
}
.header_two ul {
  width: 1200px;
  height: 240px;
  margin: 0 auto;
  padding-top: 15px;
  padding-bottom: 30px;
}
.header_two ul li {
  float: left;
  width: 100px;
  margin-right: 10px;
}
.header_two ul li:nth-child(1) {
  margin-left: 235px;
}
.header_two ul li a {
  display: block;
  width: 100px;
  height: 30px;
  font-size: 14px;
  color: #c9c9dd;
  line-height: 30px;
  text-align: center;
}
.header_two ul li a:hover {
  color: #d9ad50;
  text-decoration: underline;
}
</style>


