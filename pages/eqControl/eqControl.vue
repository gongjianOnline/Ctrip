<template>
	<view class="eqControl-wrapper">
		<topNavigation title="设备管理" leftIcon="../../static/topNavigation/left.png" />
		<view class="eqControl-eqList-container">
			<view class="eqControl-Item">
				<view class="">
					<view class="eqControl-title">男生A栋</view>
					<view class="eqControl-info">男生宿舍6楼</view>
				</view>
				<view class="del-button-container">
					<view class="del-button">删除</view>
				</view>
			</view>
			<view class="eqControl-Item">
				<view class="">
					<view class="eqControl-title">男生A栋</view>
					<view class="eqControl-info">男生宿舍6楼</view>
				</view>
				<view class="del-button-container">
					<view class="del-button">删除</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	import topNavigation from "@/compenents/topNavigation/topNavigation.vue";
	export default {
		data() {
			return {
				
			}
		},
		components:{
			topNavigation
		},
		methods: {
			
		}
	}
</script>

<style>
.eqControl-eqList-container{
	margin-top: 100rpx;
	padding: 10rpx 10rpx;
}
.eqControl-Item{
	display: flex;
	justify-content: space-between;
	background: #fff;
	padding: 10rpx;
	margin-bottom: 16rpx;
}
.eqControl-title{
	margin-bottom: 20rpx;
	font-size: 30rpx;
}
.eqControl-info{
	color: #7f7f7f;
	font-size: 24rpx;
}
.del-button-container{
	display: flex;
	justify-content: center;
	align-items: center;
}
.del-button{
	padding: 10rpx 30rpx;
	border: 1px solid #7f7f7f;
	border-radius: 10rpx;
}
</style>
