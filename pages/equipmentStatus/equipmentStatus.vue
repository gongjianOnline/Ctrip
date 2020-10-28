<template>
	<view class="equipmentStatus-wrapper">
		<view class="equipmentStatus-view-container">
			<topNavigation title="设备状态" leftIcon="../../static/topNavigation/left.png" />
			<view class="equipmentStatus-determinant">
				<view class="equipmentStatus-determinant-item">
					<indexEchar title="剩余水量" :value="0.25" elemId="surplusAmount" symbol="%"></indexEchar>
				</view>
				<view class="equipmentStatus-determinant-item">
					<indexEchar title="水质" :value="0.26" elemId="waterquality" symbol=""></indexEchar>
				</view>
			</view>
			<view class="equipmentStatus-trend-container">
				<view class="equipmentStatus-trend-content">
					<trend></trend>
				</view>
			</view>
			<view class="equipmentStatus-selec-container">
				<picker @change="PickerChange" :value="index" :range="picker">
					<view class="picker">
						当前设备：{{picker[index]}}
					</view>
				</picker>
			</view>
		</view>
	</view>
</template>

<script>
	import topNavigation from "@/compenents/topNavigation/topNavigation.vue";
	import indexEchar from "../../compenents/indexEchar/indexEchar.vue";
	import trend from "../../compenents/trend/trend.vue";
	export default {
		data() {
			return {
				index: 0,
				picker: ['男生宿舍A栋', '女生宿舍B栋'],
			}
		},
		components: {
			topNavigation,
			indexEchar,
			trend
		},
		methods: {
			confirm(e){
				console.log(e)
			},
			PickerChange(e) {
				this.index = e.detail.value
			},
		},
	}
</script>

<style scoped>
	.equipmentStatus-wrapper {
		display: flex;
		flex-direction: column;
		width: 750rpx;
		height: 100%;
	}
	.equipmentStatus-view-container {
		flex-grow: 1;
		background-image: url(../../static/index/bgImg.png);
		background-size: 750rpx;
		background-repeat: no-repeat;
	}

	.equipmentStatus-determinant {
		margin-top: 100upx;
		width: 750upx;
		height: 500upx;
		display: flex;
		align-items: center;
	}

	.equipmentStatus-determinant-item {
		width: 50%;
		height: 300upx;
	}

	.equipmentStatus-trend-container {
		width: 750upx;
		height: 400upx;
		margin-top: 100upx;
		display: flex;
		align-items: center;
	}

	.equipmentStatus-trend-content {
		width: 750upx;
		height: 400upx;
	}

	.equipmentStatus-selec-container {
		margin: 0 auto;
		width: 450upx;
		height: 50upx;
		border: 1px solid rgb(25, 118, 234);
		border-radius: 100upx;
		text-align: center;
	}
</style>
