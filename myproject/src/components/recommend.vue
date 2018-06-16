<template>
	<div class="recommend">
		<h3 div class="title">推荐商品</h3>
		<div class="content">
			<div class="content-item" v-for="(item,index) in items" :key="index">
				<img src="../../static/carousel1.png"/>
				<p class="name">
					高端衣服
				</p>
				<p class="price">
					<span class="price-now">$100</span>
					<span class="price-before">$150</span>
				</p>
				<div class="iconfont">&#xe6e7;</div>
			</div>
		</div>
	</div>
</template>

<script>
	export default{
		name: "recommend",
		data(){
			return{
				items: [{},{}]
			};
		},
		mounted(){

		}
	};
</script>

<style lang="less" scoped>
.iconfont {
	background: black;
	width: 50px;
	height: 50px;
	font-size: 25px;
	color: red;
}

	.recommend{
		background: #eee;
		display: block;
		margin: 0 auto;

		.title {
			color: gray;
			line-height: 35px;
			text-align: 35px;
		}

		.content {
			width: 100%;

			.content-item {
				float: left;
				padding-left: 20px;
				padding-right: 15px;

				img {
					width: 169px;
					height: 150px;
				}
			}

			.name {
				font-size: 15px;
				color: black;
				height: 20px;
				line-height: 20px;
				text-align: center;
			}

			.price {
				font-size: 15px;
				height: 20px;
				line-height: 20px;
				text-align: center;	

				.price-now {
					color: red;
				}

				.price-before {
					color: black;
					text-decoration: line-through;
				}			
			}
		}

        
	}
</style>