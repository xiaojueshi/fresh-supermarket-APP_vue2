<template>
	<view class="commodity-switch-component">
		<view class="commodity-switch-component__tab flex-center">
			<view class="commodity-switch-component__tab___item flex-center" v-for="(item,index) in tagData"
				:key="index+item.id" @click="switchTab(index)"
				:class="{'commodity-switch-component__tab___item-select':tagIndex===index}">
				<h1>{{item.title}}</h1>
				<h2>{{item.submit}}</h2>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				tagIndex: 0,
				tagData: [{
						id: 0,
						title: "全部",
						submit: "猜你喜欢"
					},
					{
						id: 1,
						title: "时令",
						submit: "当季优选"
					},
					{
						id: 2,
						title: "进口",
						submit: "国际直采"
					},
					{
						id: 3,
						title: "人气",
						submit: "大家在买"
					},
				]
			};
		},
		methods: {
			switchTab(index) {
				this.tagIndex = index
			}
		}
	}
</script>

<style lang="scss" scoped>
	.commodity-switch-component {
		width: 750rpx;

		.commodity-switch-component__tab {
			justify-content: space-between;
			padding: 0 20rpx;

			.commodity-switch-component__tab___item {
				position: relative;
				flex-direction: column;
				width: 187.5rpx;

				h1 {
					font-size: 30rpx;
					color: #333333;
				}

				h2 {
					margin-top: 5rpx;
					font-size: 22rpx;
					color: #999999;
				}
			}

			.commodity-switch-component__tab___item::after {
				content: "";
				width: .5rpx;
				height: 40rpx;
				background-color: #999999;
				position: absolute;
				top: 0;
				right: 0;
				transform: translateY(60%);
			}

			.commodity-switch-component__tab___item:last-child::after {
				width: 0;
			}

			.commodity-switch-component__tab___item-select {
				h1 {
					color: #40AE36;
				}

				h2 {
					color: #FFFFFF;
					background-color: #40AE36;
					padding: 5rpx 10rpx;
					border-radius: 30rpx;
				}
			}
		}
	}
</style>
