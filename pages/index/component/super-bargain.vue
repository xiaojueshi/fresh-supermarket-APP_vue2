<template>
	<view class="super-bargain-component">
		<view class="super-bargain__top flex-center">
			<view class="title flex-center">
				<h3>超划算</h3>
				<text>冬日礼遇</text>
			</view>

			<text>查看全部</text>
		</view>

		<view class="super-bargain-content flex-center">
			<view class="super-bargain-content__item flex-center" v-for="(item,index) in commodityData"
				:key="index+item.id">
				<image :src="item.imageUrl" mode=""></image>
				<text>{{item.title}}</text>
				<view class="super-bargain-content__function flex-center">
					<view class="price">
						￥
						<h3>{{item.price}}</h3>
					</view>
					<image src="../../../static/icons/购物车按钮.png" mode=""></image>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		props: {
			commodityData: {
				type: Array,
				default: () => {
					return [{
							id: 0,
							title: '四川爱媛38号香甜橙子',
							price: "39.9",
							imageUrl: require("../../../static/images/橙子.png")
						},
						{
							id: 1,
							title: '山养黄牛腱子肉',
							price: "39.9",
							imageUrl: require("../../../static/images/牛肉.png")
						},
						{
							id: 2,
							title: '有机水果卷心菜',
							price: "39.9",
							imageUrl: require("../../../static/images/卷心菜.png")
						},
					]
				}
			}
		},
		data() {
			return {

			};
		}
	}
</script>

<style lang="scss" scoped>
	.super-bargain-component {
		padding: 20rpx 30rpx;
		width: 690rpx;
		height: 390rpx;
		background-color: #FFFFFF;
		border-radius: 30rpx;

		.super-bargain__top {
			width: 100%;
			height: 40rpx;
			justify-content: space-between;

			.title {
				justify-content: left;

				h3 {
					font-size: 30rpx;
					color: #333333;
					margin-right: 10rpx;
				}

				text {
					padding: 2rpx 7rpx;
					font-size: 16rpx;
					color: #FFFFFF;
					background-color: #EC9F09;
					border-radius: 5rpx;
				}
			}

			text {
				font-size: 24rpx;
				color: #40AE36;
			}
		}

		.super-bargain-content {
			justify-content: space-between;
			padding: 20rpx 0rpx;
			width: 100%;

			.super-bargain-content__item {
				width: 170rpx;
				flex-direction: column;

				image {
					width: 164rpx;
					height: 164rpx;
				}

				text {
					font-size: 24rpx;
					color: #666666;
					width: 100%;
					white-space: nowrap;
					overflow: hidden;
					text-overflow: ellipsis;
				}
				
				.super-bargain-content__function{
					margin-top: 20rpx;
					justify-content: space-between;
					width: 100%;
					
					.price{
						color: #F55726;
						font-size: 22rpx;
						
						h3{
							font-size: 33rpx;
							display: inline-block;
						}
					}
					
					image{
						width: 44rpx;
						height: 44rpx;
					}
					
				}
			}
		}
	}
</style>
