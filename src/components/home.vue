<template>
  <div class="home">
   <v-header></v-header>
    <div class="warpper">
      <div class="content">
        <a href="#" title="查看详情"></a>
      </div>
      <div class="main">
        <div class="main_top">
          <div class="rotate">
            <ul :style="{left:num}">
              <li v-for="item in list" :key="item.title">
                <img :src="item.src">
              </li>
            </ul>
            <div class="box">
              <span
                :class="{'active':nowIndex==index}"
                @mouseover="tab(index)"
                v-for="(item,index) in list"
                :key="item.title"
              >{{item.title}}</span>
            </div>
          </div>
          <div class="cont">
            <div class="cont_a">
               <div class="dao">
                 <p :class="{'active_a':nowIndex1==index}" @mouseover="tab2(index)"
                 v-for="(item,index) in dataList.list" :key="index">{{item.title}}</p>
                 <p>...</p>
               </div>
               <div class="item_a" :style="{left:num1}">
                  <div class="item" v-for="(item,index) in dataList.list" :key="index">
                    <div class="cont_c">
                      <p><a href="#">{{item.name}}</a></p>
                      <ul>
                        <li v-for="(option,index) in item.infoList" :key="index">
                          <span class="biaoti"><a href="#">{{option.text}}</a></span>
                          <span class="tim">{{option.time}}</span>
                        </li>
                      </ul>
                    </div>
                  </div>
               </div>
            </div>
          </div>
          <div class="download_pannel">
              <a href="#" class="download_btn"></a>
              <a href="#" class="guard_btn"></a>
              <a href="#" class="tiyan_btn"></a>
            </div>
        </div>
      <div class="quick_entrance">
          <a href="#"><img src="../assets/img/zhou.jpg" alt=""></a>
          <a href="#"><img src="../assets/img/zhu.jpg" alt=""></a>
          <a href="#"><img src="../assets/img/li.jpg" alt=""></a>
          <a href="#"><img src="../assets/img/kpl.jpg" alt=""></a>
      </div>
      <div class="clearfix">
            <div class="strategy_center fl">
                <div class="item_header">
                  <h3 class="item_title">内容中心</h3>
                  <a href="#" class="more_btn fr">更多</a>
                </div>
                <div class="item_subnav">
                    <a href="#">精品栏目</a>
                    <span class="split"></span>
                    <a href="#">赛事精品</a>
                    <span class="split"></span>
                    <a href="#">英雄攻略</a>
                </div>
                <div class="item_thirdnav0">
                  <div class="title">
                    <a href="#" @mouseover="handleDataList(index)" v-for="(item,index) in itemtitle" :key="index" :class="{'on':listIndex==index}">{{item.name}}</a>
                  </div>
                </div>
                <div class="item_content">
                  <ul class="video_list ">
                    <li v-for="(item,index) in nowData.tab" :key="index">
                      <a href="#">
                        <span class="video_one"><img :src="item.src" /></span>
                        <span class="clearfix ">
                          <em class="fl ico-play">{{item.clicknumber}}</em>
                          <em class="fr">{{item.time}}</em>
                        </span>
                        <span class="video-tit">{{item.title}}</span>
                      </a>
                    </li>
                  </ul>
                </div>
            </div>
        <div class="skin_center fl" v-changeTab>
          <div class="item_header">
            <h3 class="item_titletwo">英雄/皮肤</h3>
            <a href="#" class="more_btn fr">更多</a>
          </div>
          <div class="item_subnavs">
            <a href="javascript:;">最近英雄</a>
            <span class="split"></span>
            <a href="javascript:;">最新皮肤</a>
            <span class="split"></span>
            <a href="javascript:;">周免英雄</a>
          </div>
          <div class="item_contens fl">
            <div class="item_conten fl">
              <div class="item_down">
                <a href="#"><img src="../assets/img/yunzhongjun.jpg" alt=""></a>
                <div class="new_hero_bottom">
                  <p class="new_hero_name">新英雄：云中君</p>
                  <p>上线时间：2019-05-11</p>
                </div>
              </div>
              <div class="item_up">
                <ul>
                  <li>
                    <a href="#"><img src="../assets/img/yao.jpg" alt=""></a>
                    <span class="item_zi">瑶</span>
                  </li>
                  <li>
                    <a href="#"><img src="../assets/img/pangu.jpg" alt=""></a>
                    <span class="item_zi">盘古</span>
                  </li>
                  <li>
                    <a href="#"><img src="../assets/img/zhubajie.jpg" alt=""></a>
                    <span class="item_zi">猪八戒</span>
                  </li>
                  <li>
                    <a href="#"><img src="../assets/img/change.jpg" alt=""></a>
                    <span class="item_zi">嫦娥</span>
                  </li>
                </ul>
              </div>
            </div>
            <div class="item_conten fl">
              <div class="item_down">
                <a href="#"><img src="../assets/img/lvbu.jpg" alt=""></a>
                <div class="new_hero_bottom">
                  <p class="new_hero_name">新皮肤：吕布-野性能量</p>
                  <p>上线时间：2019-06-14</p>
                </div>
              </div>
              <div class="item_up">
                <ul>
                  <li>
                    <a href="#"><img src="../assets/img/peiqinhu.jpg" alt=""></a>
                    <span class="item_zi">瑶</span>
                  </li>
                  <li>
                    <a href="#"><img src="../assets/img/xiaoqiao.jpg" alt=""></a>
                    <span class="item_zi">盘古</span>
                  </li>
                  <li>
                    <a href="#"><img src="../assets/img/jialuo.jpg" alt=""></a>
                    <span class="item_zi">猪八戒</span>
                  </li>
                  <li>
                    <a href="#"><img src="../assets/img/niumo.jpg" alt=""></a>
                    <span class="item_zi">嫦娥</span>
                  </li>
                </ul>
              </div>
            </div>
            <div class="item_conten fl">
              <div class="item_thr fl">
                <ul>
                  <li>
                    <a href="#"><img src="../assets/img/zhongkui.jpg" alt=""></a>
                    <span class="item_zi">钟馗</span>
                  </li>
                  <li>
                    <a href="#"><img src="../assets/img/ganjiang.jpg" alt=""></a>
                    <span class="item_zi">干将莫邪</span>
                  </li>
                  <li>
                    <a href="#"><img src="../assets/img/dianwei.jpg" alt=""></a>
                    <span class="item_zi">典韦</span>
                  </li>
                  <li>
                    <a href="#"><img src="../assets/img/luban.jpg" alt=""></a>
                    <span class="item_zi">鲁班</span>
                  </li>
                  <li>
                    <a href="#"><img src="../assets/img/zhuangzhou.jpg" alt=""></a>
                    <span class="item_zi">庄周</span>
                  </li>
                  <li>
                    <a href="#"><img src="../assets/img/chengyaojin.jpg" alt=""></a>
                    <span class="item_zi">程咬金</span>
                  </li>
                  <li>
                    <a href="#"><img src="../assets/img/yunzhong.jpg" alt=""></a>
                    <span class="item_zi">云中君</span>
                  </li>
                  <li>
                    <a href="#"><img src="../assets/img/gengduo.jpg" alt=""></a>
                    <span class="item_zi"></span>
                  </li>
                </ul>
              </div>
              <p class="icon_watchs fr"><span class="icon_watch">限免时间：</span><em>2019-6-24至2019-6-30</em></p>
            </div>
          </div>
          
        <div>
            </div>  
        </div>                  
      </div>
      </div>
    </div>
  </div>
</template>
<script>
import vHeader from './header.vue'
export default {
  components:{
    vHeader
  },
  data() {
    return {
      dataList: require("../assets/data/datalist.json"),
      wangdata: require("../assets/data/wangdata.json"),
      nowData: '',
      listIndex: 0,
      list: [
        {
          title: "夏日全新版本",
          src: require("../assets/img/01.jpg")
        },
        {
          title: "妮维雅王者洁面",
          src: require("../assets/img/02.jpg")
        },
        {
          title: "走进稷下学宫",
          src: require("../assets/img/03.jpg")
        },
        {
          title: "微赛事公会赛",
          src: require("../assets/img/04.jpg")
        },
        {
          title: "猫神人物志",
          src: require("../assets/img/05.jpg")
        }
      ],
      itemtitle:[
        {
          name:"最新"
        },
        {
          name:"百星王者带你飞"
        },
        {
          name:"峡谷情报局"
        },
        {
          name:"零度王者视角"
        },
        {
          name:"峡谷重案组第三季"
        },
        {
          name:"王者克制论"
        },
        {
          name:"上分拍档"
        }
      ],
      imgList: [],
      nowIndex: 0,
      num: 0,
      nowIndex1:0,
      nowIndex2:0,
      num1:0
    };
  },
  methods: {
    tab(i) {
      this.nowIndex = i;
      this.num = this.nowIndex * -604 + "px";
    },
    tab2(k){
      this.nowIndex1 = k;
      this.num1 = this.nowIndex1 * -360 + "px";
    },
    handleDataList(i){
      this.listIndex = i;
      this.nowData = this.wangdata.data[i];
    },
    tab3(j){
      this.nowIndex2 = j;
    }
  },
  created(){
    this.nowData = this.wangdata.data[0];
  },
  mounted() {
    setInterval(() => {
      this.nowIndex++;
      this.nowIndex = this.nowIndex > 4 ? 0 : this.nowIndex;
      this.num = this.nowIndex * -604 + "px";
    }, 3000);
  },
  directives:{
    changeTab:{
      bind(el){
        let tabList=el.querySelectorAll(".item_subnavs a");
        let conts = el.querySelector(".item_contens");
        tabList.forEach((item,index)=>{
            item.addEventListener("mouseover",function(){
              conts.style.left=(-295*index)+"px";
            })
        })
      }
    }
  }
};
</script>
<style>
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
.fl{
  float: left;
}
.fr{
  float:right;
}
.wrapper {
  position: relative;
}
.content {
  width: 100%;
  height: 1075px;
  position: absolute;
  left: 0;
  top: 127px;
  background: url(../assets/img/back.jpg);
  background-size: 100% 1100px;
}
.content a {
  width: 199px;
  height: 60px;
  position: absolute;
  top: 458px;
  left: 690px;
}
.main {
  width: 1200px;
  padding-top: 590px;
  margin: 0 auto;
}
.main_top {
  width: 1200px;
  height: 342px;
  position: relative;
  background: url(../assets/img/rotate_bg.png) no-repeat;
}
.main_top .rotate {
  width: 604px;
  height: 342px;
  overflow: hidden;
  float: left;
}
.main_top .rotate ul {
  width: 3020px;
  height: 298px;
  position: relative;
  left: 0;
  top: 0;
  transition: 0.5s;
}
.main_top .rotate ul li {
  width: 604px;
  height: 298px;
  float: left;
}
.main_top .box {
  width: 100%;
  cursor: pointer;
}
.main_top .box span {
  float: left;
  display: block;
  width: 120.8px;
  height: 44px;
  line-height: 44px;
  font-size: 14px;
  text-align: center;
  color: #b1b2be;
}
.main_top .box .active {
  background: rgba(255, 255, 255, 0.15);
  color: #f3c258;
}
.cont {
  width: 360px;
  float: left;
  overflow: hidden;
}
.cont  .cont_a .dao .active_a{
  color: #f3c258;
  color: #f3c258;
  border-bottom: 3px solid #f3c258;
}
.cont_b {
  width: 325px;
  height: 45px;
  margin: 0 auto;
  border-bottom: 1px solid #000;
}
.cont_b li {
  width: 52px;
  height: 45px;
  text-align: center;
  line-height: 45px;
  color: #b8b9c5;
  font-size: 14px;
  float: left;
}
.cont .cont_a .item_a{
  width: 1800px;
  position: relative;
  left: 0;
  transition: .3s ease-in;
}
.cont .cont_a .dao{
  width: 325px;
  height: 50px;
  cursor: pointer;
  line-height: 50px;
  margin: 0 27px;
  border-bottom: 1px solid #000;
}
.cont .cont_a .dao p{
  float: left;
  width: 52px;
  height: 46px;
  font-size: 14px;
  color: #b8b9c5;
  text-align: center;
}
.cont .cont_a .item{
  width: 360px;
  float: left;
}
.cont_c ul{
  width: 325px;
  margin: 0 auto;
}
.cont_c p{
  width: 325px;
  height: 36px;
  background: #414046;
  text-align: center;
  line-height: 36px;
  margin: 20px auto;
  color: #f3c258;
  font-size: 18px;
}
.cont_c p a{
  color: #f3c258;
  font-size: 18px;
  display: block;
  width: 280px;
  padding-left: 10px;
  text-overflow: ellipsis;
  white-space: nowrap;
  overflow: hidden;
}
.cont_c p a:hover{
  text-decoration: underline;
}
.cont_c li {
  width: 325px;
  cursor: pointer;
  margin-bottom: 10px;
}
.cont_c .biaoti a{
  text-overflow: ellipsis;
  white-space: nowrap;
  overflow: hidden;
  color: #b8b9c5;
  font-size: 14px;
  float: left;
  width: 275px;
}
.cont_c .biaoti a:hover{
  text-decoration: underline;
}
.cont_c .tim{
  color: #999;
  font-size: 12px;
  margin-left: 16px;
}
.download_pannel{
  width: 236px;
  height: 342px;
  float: left;
  overflow: hidden;
  position: relative;
}
.download_pannel a{
    background: url(../assets/img/xuebi.png);
    display: block;
}
.download_pannel .download_btn{
  display: block;
  width: 236px;
  height: 128px;
  background-position: 0 -219px;
}
.download_pannel .guard_btn{
  width: 236px;
  height: 106px;
  background-position: 0 -350px;
}
.download_pannel .tiyan_btn{
  width: 236px;
  height: 108px;
  background-position: 0 -461px;
}
.quick_entrance{
  width: 1200px;
  height: 134px;
  position: relative;
  font-size: 0;
  margin: 28px auto 34px;
}
.quick_entrance a{
  display: inline-block;
  width: 291px;
  height: 134px;
  margin-right: 12px;
  overflow: hidden;
}
.quick_entrance a:nth-last-child(1){
  margin-right: 0;
}
.quick_entrance a img{
  transition: .5s;
}
.quick_entrance a img:hover{
  transform: scale(1.1);
}
.strategy_center{
  width: 872px;
  height: 528px;
  margin-right: 33px;
}
.item_header{
  position: relative;
  margin-bottom: 16px;
}
.item_title{
  background: url(../assets/img/xuebi.png) no-repeat;
  background-position: 0 -106px;
  width:140px;
  height: 26px;
  text-indent: 2rem;
  line-height: 25px;
  font-size: 22px;
  font-weight: bold;
  letter-spacing: 1px;
  display: inline-block;
}
.more_btn{
    /* position: absolute;
    top: 0;
    right: 0; */
    padding-left: 22px;
    background: url(../assets/img/xuebi.png)no-repeat -252px 4px;
    color: #999;
}
.item_subnav{
  position: relative;
  width: 872px;
  height:32px;
  line-height: 32px;
  background: #f5f5f5;
  margin-bottom: 5px;
}
.item_subnav a{
  width: 289px;
  display: block;
  float: left;
  text-align: center;
  font-size: 14px;
  color: #999;
}
.split{
  width: 1px;
  height: 20px;
  overflow: hidden;
  float: left;
  background: #e1e1e1;
  display: inline-block;
  margin: 5px 0 0px;
}
.item_thirdnav0{
  height: 26px;
  line-height: 26px;
  padding: 8px 0 9px;
}
.item_thirdnav0 .title{
  text-indent: 8px;
  cursor: pointer;
  height:26px;
  overflow:hidden;
}
.item_thirdnav0 .title a{
  height: 24px;
  line-height:24px;
  padding:0 13px 0 8px;
  border:1px solid #e5e5e5;
  font-size: 14px;
  color:#000;
  background: #f5f5f5;
  border-radius: 10px;
  display: block;
  float: left;
  margin-right: 8px;
}
.item_content ul li{
  position: relative;
  width:209px;
  margin: 0 12px 30px 0;
  float:left;
}
.item_content ul li>a{
  display: block;
}
.item_content .video_one{
  display: block;
  height: 125px;
  position: relative;
}
.item_content .video_one:hover:before{
  content: "";
  width: 209px;
  height: 125px;
  background:rgb(0,0,0,0.5);
  position: absolute;
  z-index: 2;
  top: 0;
  left: 0;
}
.item_content .video_one:hover:after{
  content: "";
  width: 44px;
  height: 45px;
  background: url(../assets/img/xuebi.png) no-repeat;
  background-position:-190px -60px;
  position: absolute;
  z-index: 5;
  top: 30px;
  left: 80px;
}
.item_content ul li:nth-child(4n){
  margin-right: 0;
}
.item_content .clearfix{
  position:absolute;
  top:103px;
  left: 0;
  background: rgba(0, 0, 0, 0.6);
  width: 189px;
  height: 22px;
  line-height: 22px;
  color: #fff;
  padding:0 10px;
  font-size: 12px;
}
.video_list img{
  width:209px;
  height: 125px;
}
.item_content .clearfix .ico-play{
  background:url(../assets/img/xuebi.png) no-repeat;
  display: inline-block;
  padding-left: 15px;
  background-position:-255px -59px;
}
.video-tit{
    display: block;
    height: 40px;
    overflow: hidden;
    color: #333333;
    margin-top: 10px;
    font-size: 14px;
}
.item_thirdnav0 .title .on{
  background: #f3c258;
  color: #fff;
}
.item_titletwo{
  background: url(../assets/img/xuebi.png) no-repeat;
  background-position: 0 -143px;
  width:140px;
  height: 26px;
  text-indent: 2rem;
  line-height: 25px;
  font-size: 22px;
  font-weight: bold;
  letter-spacing: 1px;
  display: inline-block;
}
.item_subnavs{
    position: relative;
    width: 295px;
    height: 32px;
    line-height: 30px;
    background: #f5f5f5;
    margin-bottom: 19px;
}
.item_subnavs a{
    width: 97px;
    display: block;
    float: left;
    text-align: center;
    font-size: 14px;
    color: #999;
}
.item_subnavs a:hover{
  border-bottom: 2px solid #f3c258;
  color: #000;
}
.item_down{
  width: 295px;
  height: 224px;
  margin-bottom: 10px;
}
.item_down .new_hero_bottom{
  width: 295px;
  height: 68px;
  border: 1px solid #e5e5e5;
  border-top:none;
  margin-top: -5px;
  border-radius: 2px; 
  padding: 10px 15px;
  box-sizing: border-box;
}
.item_down .new_hero_name{
  font-size: 18px;
  color: #333333;
  font-weight: bold;
}
.new_hero_bottom p{
  color: #999999;
  font-size: 12px;
}
.skin_center{
  width: 295px;
  overflow: hidden;
  position: relative;
  height: 500px;
}
.item_conten{
  width: 295px;
}
.item_contens{
  width: 885px;
  position: absolute;
  left: 0;
  top: 90px;
  transition: .5s; 
}
.item_up ul li{
  float: left;
  margin-right: 7px;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
}
.item_up ul li:nth-last-child(1){
  margin-right: 0;
}
.item_up ul li:hover:before{
  content: "";
  width: 68px;
  height: 177px;
  background:rgba(0,0,0,0.9);
  position: absolute;
  top: 0;
  left: 0;
}
.item_up ul li:hover .item_zi{
  display: block;
}
.item_up .item_zi{
  width: 20px;
  display: none;
  position: absolute;
  color: #f3c258;
  font-size: 14px;
  padding-left: 2px;
}
.item_thr ul li{
  float: left;
  margin-right: 7px;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  margin-bottom: 10px;
}
.item_thr ul li:nth-child(4n){
  margin-right: 0;
}
.item_thr ul:not(li:last-child):hover:before{
  content: "";
  width: 68px;
  height: 177px;
  background:rgba(0,0,0,0.9);
  position: absolute;
  top: 0;
  left: 0;
}
.item_thr ul li:hover .item_zi{
  display: block;
}
.item_thr .item_zi{
  width: 20px;
  display: none;
  position: absolute;
  color: #f3c258;
  font-size: 14px;
  padding-left: 2px;
}
.item_conten .icon_watchs{
  color: #999999;
  font-size: 12px;
  text-align: right;
  position: relative;
}
.item_conten .icon_watch:before{
  content: "";
  position: absolute;
  background: url(../assets/img/xuebi.png);
  background-position: -659px -42px;
  width: 14px;
  height: 14px;
  top: 2px;
  left: -23px;
  
}
</style>


