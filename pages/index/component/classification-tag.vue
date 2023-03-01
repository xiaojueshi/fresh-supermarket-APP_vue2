<template>
	<view class="classification-tag-component flex-center">
		<view class="classification-tag__item flex-center" v-for="(item,index) in classificationTag" :key="index">
			<image :src="item.icon" mode=""></image>
			<text>{{item.title}}</text>
		</view>
	</view>
</template>

<script>
	export default {
		props: {
			classificationTag: {
				type: Array,
				default: () => {
					return [{
							title: "水果蔬菜类",
							icon: require("../../../static/icons/水果蔬菜.png")
						},
						{
							title: "肉禽蛋品类",
							icon: require("../../../static/icons/肉禽蛋品.png")
						},
						{
							title: "速食冷冻类",
							icon: require("../../../static/icons/速食冷冻.png")
						},
						{
							title: "海鲜水产类",
							icon: require("../../../static/icons/海鲜水产.png")
						},
						{
							title: "粮油米面类",
							icon: require("../../../static/icons/粮油米面.png")
						}
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
	.classification-tag-component {
		width: 690rpx;
		height: 160rpx;
		justify-content: space-between;

		.classification-tag__item {
			flex-direction: column;
			
			image{
				width: 108rpx;
				height: 108rpx;
			}
			
			text{
				font-size: 24rpx;
				color: #666666;
				margin-top: 10rpx;
			}
		}
	}
</style>
