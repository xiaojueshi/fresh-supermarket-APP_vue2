<template>
	<view class="recommend-component flex-center">
		<component-recommend v-for="(item,index) in recommendData" :key="index" :title="item.title"
			:subtitle="item.subtitle" :image1="item.images1" :image2="item.images2"></component-recommend>
	</view>
</template>

<script>
	export default {
		props: {
			recommendData: {
				type: Array,
				default: () => {
					return [{
							title: "吃好点",
							submit: "美国小木瓜尝鲜",
							images1: require("../../../static/images/西兰花.png"),
							images2: require("../../../static/images/罗汉果.png")
						}, {
							title: "产地量贩",
							submit: "核桃19.9元/箱",
							images1: require("../../../static/images/核桃.png"),
							images2: require("../../../static/images/螃蟹.png")
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
	.recommend-component{
		width: 690rpx;
		justify-content: space-between;
	}
</style>
