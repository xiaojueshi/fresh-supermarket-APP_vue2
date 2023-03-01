<template>
	<view class="content">
		<view class="window-top" :style="{background:backgroundColor}"></view>
		<slot></slot>
	</view>
</template>

<script>
	export default {
		props: {
			backgroundColor: {
				type: String,
				default: "#F8F9FA"
			}
		},
		data() {
			return {

			};
		}
	}
</script>

<style lang="scss" scoped>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		padding-bottom: 20rpx;

		.window-top {
			width: 750rpx;
			height: var(--status-bar-height);
			position: -webkit-sticky;
			position: sticky;
			top: 0px;
			z-index: 999;
		}
	}
</style>
