<template>
	<view class="banner-component">
		<image src="../../../static/images/banner.png" mode="widthFix"></image>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			};
		}
	}
</script>

<style lang="scss" scoped>
	.banner-component{
		width: 690rpx;
		height: 240rpx;
		border-radius: 25rpx;
		background-color: $uni-color;
		overflow: hidden;
		
		image{
			width: 100%;
			height: 100%;
		}
	}
</style>
