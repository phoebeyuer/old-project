<template>
    <div class="test">
    	<!-- 动态路由 -->
	     this is id : {{$route.params.testId}}

		 <!-- 嵌套路由 -->
		 <router-link to="/test/title1">标题1</router-link>
		 <router-link to="/test/title2">标题2</router-link>
		 <router-view></router-view>

		 <!-- 编程式路由 -->
		 <div @click="gotoGoods">跳转到商品详情页面</div>    <!-- 点击后实现gotoGoods方法 -->

		 <router-link v-bind:to="{name:'goods'}">用命名路由的方式跳转到商品详情页</router-link>
	</div>
</template>

<script>
     export default{
	     data(){
		     return{
			     msg:'hello vue'
			 }
		 },
		 methods:{
		 	 gotoGoods(){
		 		// this.$router.push('/goods');      //编程式路由实现跳转
/*		 		this.$router.push({                  //携带参数实现跳转方法1
		 			path: '/goods?goodId=666'
		 		});*/
		 		this.$router.push({            //携带参数实现跳转方法2
		 			path: '/goods',
		 			query:{
		 				goodsId:666
		 			}
		 		});
	 	     }
	 	 }
	 }
	 
</script>

<style scoped>
</style>