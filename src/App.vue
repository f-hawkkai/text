<template>
  <div id="app">
    <!-- <img src="./assets/logo.png"> -->
    <router-view/>
         
  </div>
</template>

<script>
 import Home from './components/Home'
  export default {
      name:"App",
      components:{
        Home
      },
      created:function(){
          console.log("组件创建完成")
      }
  }
</script>
   
<style>
</style>
