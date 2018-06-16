<template>
  <div class="myHeader">
    <div class="headerImg">
      <img :src="imgHeader"/>
    </div>
    <div class="headerTxt">Phoebe-Luxury Store</div>
  </div>
</template>

<script>
  export default{
    name:"myHeader",
    data(){
      return{
        // msg: "Welcome to Your Vue.js App"
        imgHeader: require('../img/phoebe.jpg')
      };
    }
  };
</script>

<style lang="less" scoped>
.myHeader{
  height:70px;
  background: #3a3a3a;
}

.headerImg{
  display:inline-block;
  float: left;
  padding-left:3px;
  margin-top:7px;
  width:60px;
  height:60px;
  /*border:2px solid white;*/
}

.myHeader img{
  width:50px;
  height:50px;
  border: 3px solid white;
}

.headerTxt{
  width:255px;
  height:70px;
  line-height: 70px;
  
}
  
</style>