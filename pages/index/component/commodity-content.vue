<template>
	<view class="commodity-content-component flex-center">
		<view class="commodity-content-left commodity-content">
			<component-commodity-content-item v-for="(item,index) in commodityLeft" :key="index+item.id"
				:commodity-data="item"></component-commodity-content-item>
		</view>

		<view class="commodity-content-right commodity-content">
			<component-commodity-content-item v-for="(item,index) in commodityRight" :key="index+item.id"
				:commodity-data="item"></component-commodity-content-item>
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
							type:0,
							imageUrl: require("../../../static/images/菠菜1.png"),
							title: "彩食鲜菠菜 270g/份",
							labels: [{
									title: "特价",
									color: "#F55726"
								},
								{
									title: "24H发货",
									color: "#40AE36"
								},
							],
							price: "12.8",
							units: "份"
						},
						{
							id: 1,
							type:0,
							imageUrl: require("../../../static/images/橙子.png"),
							title: "四川爱媛38号可吸果冻橙子 1kg/份",
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
							units: "箱"
						},
						{
							id: 2,
							type:0,
							imageUrl: require("../../../static/images/胡萝卜.png"),
							title: "云南昆明 有机水果胡萝卜 1.5kg/份",
							labels: [{
									title: "特价",
									color: "#F55726"
								},
								{
									title: "24H发货",
									color: "#40AE36"
								},
							],
							price: "38.8",
							units: "箱"
						},
						{
							id: 2,
							type:1,
							imageUrl: require("../../../static/images/广告位.png"),
							title: "云南昆明 有机水果胡萝卜 1.5kg/份",
							labels: [{
									title: "特价",
									color: "#F55726"
								},
								{
									title: "24H发货",
									color: "#40AE36"
								},
							],
							price: "38.8",
							units: "箱"
						},
						{
							id: 3,
							type:0,
							imageUrl: require("../../../static/images/核桃.png"),
							title: "云南香格里拉 野生山核桃 原味150g*6",
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
							units: "箱"
						},
						{
							id: 4,
							type:0,
							imageUrl: require("../../../static/images/菠菜2.png"),
							title: "彩食鲜菠菜 270g/份",
							labels: [{
									title: "特价",
									color: "#F55726"
								},
								{
									title: "24H发货",
									color: "#40AE36"
								},
							],
							price: "12.8",
							units: "份"
						},
					]
				}
			}
		},
		data() {
			return {
				commodityLeft: [],
				commodityRight: []
			};
		},
		mounted() {
			if (this.commodityData.length !== 0) {
				this.cutCommodityData(this.commodityData)
			}
		},
		watch: {
			commodityData: {
				handler(val) {
					this.cutCommodityData(val)
				},
				deep: true
			}
		},
		methods: {
			cutCommodityData(data) {
				let left = []
				let right = []
				data.forEach((item, index) => {
					if (index % 2 === 0 || index === 0) {
						left.push({...item,index})
					} else {
						right.push(item)
					}
				})
				this.commodityLeft = left
				this.commodityRight = right
			}
		}
	}
</script>

<style lang="scss" scoped>
	.commodity-content-component {
		width: 690rpx;
		justify-content: space-between;
		align-items: flex-start;
	}

	.commodity-content-component>.commodity-content>.commodity-content-item {
		margin-top: 30rpx;
	}
</style>
