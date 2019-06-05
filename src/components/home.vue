<template>
    <div class="home">
        <div class="tou">
		<ul class="tu">
			 <li class="oli ali"><img src="../assets/img/tou.jpg" width="220" height="50px"></li>
			 <li class="oli"><img src="../assets/img/tou1.jpg"/></li>
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
				<img src="../assets/img/alogo.png"/>
			</div>
			<ul class="let">
				<li>
					<a href="#">首页
					<em>home</em>
					</a>
				</li>
				<li>
					<a href="#">游戏资料
					<em>data</em>
					</a>
				</li>
				<li>
					<a href="#">内容中心
					<em>contents</em>
					</a>
				</li>
				<li>
					<a href="#">赛事中心
					<em>match</em>
					</a>
				</li>
				<li>
					<a href="#">百态王者
					<em>culture</em>
					</a>
				</li>
				<li>
					<a href="#">社区互动
					<em>community</em>
					</a>
				</li>
				<li>
					<a href="#">玩家支持
					<em>player</em>
					</a>
				</li>
			</ul>
			<div class="login">
				<span><a href="#"><img src="../assets/img/login.png"/></a></span>
				<div class="log_in">
					<a href="#">欢迎登陆</a>
					<p>登录后查看游戏战绩</p>
				</div>
			</div>
		</div>
		
	</div>
	<div class="content">
		
	</div>
    </div>
</template>
<script>
export default{
	
}

</script>
<style>
*{
	margin: 0;
	padding: 0;
}
li{
	list-style: none;
}
em{
	font-style: normal;
}
body{
	padding-top: 42px;
	overflow-x: hidden;
}
a{
	text-decoration: none;
	color: #c9c9dd;
}
.tou{
	width: 100%;
	border-width: 1px 0;
	position: absolute;
	height: 42px;
	left: 0;
	top: 0 !important;
	border: 1px solid #c9c9c9
}
.tou .tu{
	width: 950px;
	margin: 0 auto;
}
.oli{
	float: left;
}
.ali{
	width: 205px;
    padding: 0 15px 0 0;
    background-position: 0 -40px;
    position: relative;
    z-index: 10001
}
.ol{
	float: right;
}
.zi{
	float: left;
	width: 118px;
	font-size: 12px;
	font-weight: 400;
	cursor: pointer;
	text-indent: 2rem;
	line-height: 40px;
}
.lg{
	background: url(../assets/img/logo.png) 12px no-repeat;
}
.header{
	width: 100%;
	position: absolute;
	top: 42px;
	left: 0;
	height: 85px;
	background: rgba(0,0,0,0.8);
}
.log{
	float: left;
}
.log img{
	position: absolute;
	top: 16px;
	left: 0;
}
.header-inner{
	width: 1200px;
	height: 84px;
	position: relative;
	margin: 0 auto;
}
.let{
	width: 790px;
	float: left;
	padding-left: 230px;
}
.let li{
	width: 110px;
	float: left;
	height: 84px;
	text-align: center;
}
.let li a{
	display: block;
	width: 110px;
	height: 64px;
	line-height: 30px;
	color: #c9c9dd;
	font-size: 18px;
	padding: 20px 0 0;
}
.let li a em{
	display: block;
    padding-top: 5px;
    font-size: 12px;
    line-height: 16px;
    color: #858792;
    text-transform: uppercase;
}
.login{
	width: 182px;
	position: absolute;
	right: 0;
	top: 21px;
}
.login img{
	border: 1px solid #d9ad50;
    border-radius: 42px;	
}
.login span{
	display: block;
	float: left;
}
.login .log_in{
	float: left;
	width: 130px;
	margin-left: 5px;
}
.log_in a{
	color: #fff;
}
.log_in p{
	font-size: 14px;
	color: #858792;
	padding-top: 3px;
}
.content{
	width: 100%;
	height: 1100px;
	background: url(../assets/img/back.jpg);
	background-size: 100% 1100px;
}
</style>


