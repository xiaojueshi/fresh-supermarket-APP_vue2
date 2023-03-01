<template>
	<layout-top-safety-zone background-color="#40AE36">
		<view class="page-top flex-center">
			<view class="positioning flex-center">
				<image src="../../static/icons/positioning.png" class="positioning-icon"></image>
				<text>海淀区中关村大厦</text>
				<image src="../../static/icons/下拉.png" class="positioning-icon2"></image>
			</view>

			<view class="funtion flex-center">
				<image src="../../static/icons/扫一扫.png" class="positioning-icon scan"></image>
				<image src="../../static/icons/消息.png" class="positioning-icon"></image>
			</view>
		</view>

		<view class="search-box flex-center">
			<image src="../../static/icons/搜索.png" mode=""></image>
			<text>{{searchText}}</text>
		</view>

		<view class="banner">
			<Banner></Banner>
		</view>

		<view class="classification-tag">
			<ClassificationTag></ClassificationTag>
		</view>

		<view class="super-bargain">
			<SuperBargain></SuperBargain>
		</view>

		<view class="recommend">
			<Recommend></Recommend>
		</view>

		<view class="commodity-switch">
			<CommoditySwitch></CommoditySwitch>
		</view>

		<view class="commodity-content">
			<CommodityContent></CommodityContent>
		</view>
	</layout-top-safety-zone>
</template>

<script>
	import Banner from "./component/banner.vue"
	import ClassificationTag from "./component/classification-tag.vue"
	import SuperBargain from "./component/super-bargain.vue"
	import Recommend from "./component/recommend.vue"
	import CommoditySwitch from "./component/commodity-switch.vue"
	import CommodityContent from "./component/commodity-content.vue"

	export default {
		components: {
			Banner,
			ClassificationTag,
			SuperBargain,
			Recommend,
			CommoditySwitch,
			CommodityContent
		},
		data() {
			return {
				searchText: "吃出美好生活",
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style lang="scss" scoped>
	.page-top {
		width: 750rpx;
		height: 93rpx;
		background-color: $uni-color;
		padding: 0 30rpx;
		justify-content: space-between;

		position: -webkit-sticky;
		position: sticky;
		top: var(--status-bar-height);
		z-index: 999;

		.positioning-icon {
			width: 48rpx;
			height: 48rpx;
		}

		.positioning {

			text {
				margin: 0 5rpx;
				font-size: 30rpx;
				font-weight: 600;
				color: #fff;
			}

			.positioning-icon2 {
				width: 16rpx;
				height: 9rpx;
			}
		}

		.funtion {
			.scan {
				margin-right: 20rpx;
			}
		}
	}

	.search-box {
		margin-top: 20rpx;
		width: 690rpx;
		height: 80rpx;
		background-color: #EDEFF2;
		border-radius: 50rpx;
		padding: 0 50rpx;
		justify-content: left;

		image {
			width: 33rpx;
			height: 33rpx;
			margin-right: 20rpx;
		}

		text {
			color: #999999;
			font-size: 28rpx;
		}
	}

	.banner {
		padding: 20rpx 0;
	}

	.classification-tag {}

	.super-bargain {
		margin-top: 30rpx;
	}

	.recommend {
		margin-top: 20rpx;
	}

	.commodity-switch {
		margin-top: 20rpx;
	}

	.commodity-content {
		margin-top: 20rpx;
	}
</style>
