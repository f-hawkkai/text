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
      nowIndex: 0,
      num: 0,
      nowIndex1:0,
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
    }
  },
  mounted() {
    setInterval(() => {
      this.nowIndex++;
      this.nowIndex = this.nowIndex > 4 ? 0 : this.nowIndex;
      this.num = this.nowIndex * -604 + "px";
    }, 3000);
  }
};
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
.wrapper {
  position: relative;
}
.content {
  width: 100%;
  height: 1100px;
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
</style>


