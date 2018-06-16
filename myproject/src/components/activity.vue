<template>
	<div class="activity">
		<h3 class="title">活动推荐</h3>
		<div class="content">
			<div class="content_item" v-for="(item,index) in items" :key="index">
				<img src="../../static/carousel3.png" alt="">
				<p class="name">品牌：Phoebe-Luxury Store</p>
				<p class="desc">这是一个秋季发布的品牌</p>
			</div>
		</div>
	</div>
</template>

<script>
	export default{
		name: "activity",
		data(){
			return{
				items: [1,2]
			};
		},
		mounted(){

		}
	};
</script>

<style lang="less" scoped>
	.activity {
		dispay: block;
		margin: 0 auto;

		.title {
			width: 100%;
			color: gray;
			line-height: 35px;
			text-align: 35px;
			background: #eee;
		}

		.content {
			.content_item {
				background-color: rgba(238,238,238,0.5);
				margin-bottom: 10px;
				img {
					width: 100%;
					height: 150px;
				}
			}

			.name {
				font-size: 15px;
				color: #000;
				margin-bottom: 5px;
			}

			.desc {
				font-size: 13px;
				color: #000;
			}

		}

	}
</style>