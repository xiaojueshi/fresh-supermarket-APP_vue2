<template>
	<view class="recommend-item-component">
		<h1>{{title}}</h1>
		<h2>{{subtitle}}</h2>
		<view class="recommend-item-component__images flex-center">
			<image :src="image1" mode=""></image>
			<image :src="image2" mode=""></image>
		</view>
	</view>
</template>

<script>
	export default {
		props: {
			title: {
				type: String,
				default: "吃好点"
			},
			subtitle: {
				type: String,
				default: "美国小木瓜尝鲜"
			},
			image1: {
				default: require("../../static/images/西兰花.png")
			},
			image2: {
				default: require("../../static/images/罗汉果.png")
			}
		},
		data() {
			return {

			};
		}
	}
</script>

<style lang="scss" scoped>
	.recommend-item-component{
		width: 334rpx;
		height: 256rpx;
		background-color: #FFFFFF;
		border-radius: 15rpx;
		padding: 20rpx 30rpx;
		
		h1{
			font-size: 30rpx;
			color: #333333;
		}
		
		h2{
			font-size: 24rpx;
			color: #999999;
		}
		
		.recommend-item-component__images{
			justify-content: space-between;
			margin-top: 20rpx;
			
			image{
				width: 130rpx;
				height: 130rpx;
			}
		}
	}

</style>
