<template>
	<view class="wrapper">
		<view class="view-container">
			<top></top>
			<view class="index-container-information">
				<image src="../../static/index/information.png" mode="" class="index-information"></image>
			</view>
			<view class="echarts-container">
				<indexEchar></indexEchar>
			</view>
			<view class="operation-container">
				<view class="operation-item" @click="menuFun('nearby')">
					<view class="operation-content">
						<image src="../../static/index/search.png" mode="" class="operation-img"></image>
					</view>
					<view class="operation-content">附近</view>
				</view>
				<view class="operation-item" @click="menuFun('')">
					<view class="operation-content">
						<image src="../../static/index/scanning.png" mode="" class="operation-img"></image>
					</view>
					<view class="operation-content">扫描</view>
				</view>
				<view class="operation-item" @click="menuFun('')">
					<view class="operation-content">
						<image src="../../static/index/see.png" mode="" class="operation-img"></image>
					</view>
					<view class="operation-content">设备状态</view>
				</view>
			</view>
		</view>
		<view class="">
			<tabBer></tabBer>
		</view>
	</view>
</template>

<script>
	import tabBer from "../../compenents/tabBer/tabBer.vue";
	import top from "../../compenents/top.vue"
	import indexEchar from "../../compenents/indexEchar/indexEchar.vue"
	export default {
		data() {
			return {
				
			}
		},
		components: {
			tabBer,
			top,
			indexEchar
		},
		methods: {
			menuFun(routerName){
				uni.navigateTo({
				    url: `../${routerName}/${routerName}`,
				    success: res => {},
				    fail: () => {},
				    complete: () => {}
				});
			}
		}
	}
</script>

<style scoped>
.wrapper{
	display: flex;
	flex-direction: column;
	width: 750rpx;
	height: 100%;
}
.view-container{
	flex-grow: 1;
	background-image: url(../../static/index/bgImg.png);
	background-size:750rpx 100%;
	background-repeat: no-repeat;
}
.index-information{
	width: 70rpx;
	height: 70rpx;
}
.index-container-information{
	text-align: right;
	margin-right: 20rpx;
}
.echarts-container{
	width: 750rpx;
	height: 350rpx;
	display: flex;
	justify-content: center;
	align-items: center;
}
.operation-container{
	margin-top: 35%;
	width: 750rpx;
	height: 200rpx;
	display: flex;	
	justify-content:space-around;
}
.operation-item{
	width:33.333%;
	height:100%;
}
.operation-img{
	width: 110rpx;
	height:110rpx;
}
.operation-content{
	text-align: center;
}

</style>
