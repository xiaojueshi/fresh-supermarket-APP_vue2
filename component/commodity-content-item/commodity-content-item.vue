<template>
	<view class="commodity-content-item">
		<view v-if="commodityData.type === 0" class="commodity-content-item-one">
			<image :src="commodityData.imageUrl" mode="widthFix"></image>

			<h1>{{commodityData.title}}</h1>

			<view class="commodity-labels">
				<text v-for="(item,index) in commodityData.labels" :key="index"
					:style="{'color':item.color,'border-color':item.color}">
					{{item.title}}
				</text>
			</view>

			<view class="commodity-price-block flex-center">
				<view class="commodity-price">
					￥
					<h3>{{commodityData.price}}</h3>
					<text>/{{commodityData.units}}</text>
				</view>

				<image src="../../static/icons/购物车按钮.png" mode=""></image>
			</view>
		</view>

		<view class="advertisement" v-if="commodityData.type === 1">
			<image :src="commodityData.imageUrl" mode=""></image>
		</view>

	</view>
</template>

<script>
	export default {
		props: {
			commodityData: {
				type: Object,
				default: () => {
					return {
						id: 1,
						imageUrl: require("../../static/images/橙子.png"),
						title: "四川爱媛38号可吸果冻橙 1kg/份",
						labels: [{
								title: "特价",
								color: "#F55726"
							},
							{
								title: "24H发货",
								color: "#40AE36"
							},
						],
						price: "39.9",
						units: "箱",
						type: 0 // 0 商品（默认）；1 广告
					}
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
	.commodity-content-item {
		width: 334rpx;
		border-radius: 25rpx;
		overflow: hidden;

		.commodity-content-item-one {
			background-color: #FFFFFF;
			padding: 20rpx;

			image {
				width: 100%;
			}

			h1 {
				font-size: 26rpx;
				color: #333333;
			}

			.commodity-labels {
				margin: 20rpx 0;

				text {
					font-size: 18rpx;
					padding: 8rpx;
					border: 1rpx solid;
					border-radius: 10rpx;
					margin-right: 10rpx;
				}
			}

			.commodity-price-block {
				justify-content: space-between;

				.commodity-price {
					font-size: 24rpx;
					color: #F55726;

					h3 {
						display: inline-block;
						font-size: 34rpx;
					}

					text {
						font-size: 25rpx;
						color: #999999;
					}
				}

				image {
					width: 55rpx;
					height: 55rpx;
				}
			}
		}
		
		.advertisement{
			image{
				width: 334rpx;
				height: 486rpx;
			}
		}
	}
</style>
