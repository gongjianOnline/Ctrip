<template>
	<view class="wrapper">
		<view class="mine-view-container">
			<top></top>
			<view class="mine-container-information">
				<image  src="../../static/mine/intercalate.png" 
						mode="" 
						class="mine-index-information"
						@click="intercalateFun"></image>
			</view>
			<view class="mine-userLogo-container">
				<image src="../../static/mine/user_logo.png" mode="" class="mine-userLogo"></image>
			</view>
			<view class="mine-userInfo-container">
				<view class="mine-userInfo-name">admin</view>
				<view class="mine-userInfo-remaining">卡内余额: 93.65元</view>
			</view>
			<view class="mine-carte-flex">
				<view class="mine-carte-container">
					<view class="mine-carte-conter" @click="carteFun('car')">
						<img src="../../static/mine/car.png" alt="" class="mine-carte-img">
						<view class="mine-carte-title">我的水卡</view>
					</view>
					<view class="mine-carte-conter" @click="carteFun('info')">
						<img src="../../static/mine/info.png" alt="" class="mine-carte-img">
						<view class="mine-carte-title">个人信息</view>
					</view>
					<view class="mine-carte-conter" @click="carteFun('admin')">
						<img src="../../static/mine/admin.png" alt="" class="mine-carte-img">
						<view class="mine-carte-title">设备管理</view>
					</view>
				</view>
				<view class="mine-carte-container">
					<view class="mine-carte-conter" @click="carteFun('record')">
						<img src="../../static/mine/record.png" alt="" class="mine-carte-img">
						<view class="mine-carte-title">打水记录</view>
					</view>
					<view class="mine-carte-conter" @click="carteFun('recharge')">
						<img src="../../static/mine/recharge.png" alt="" class="mine-carte-img">
						<view class="mine-carte-title">水卡充值</view>
					</view>
					<view class="mine-carte-conter" @click="carteFun('rechargeRecord')">
						<img src="../../static/mine/rechargeRecord.png" alt="" class="mine-carte-img">
						<view class="mine-carte-title">充值记录</view>
					</view>
				</view>
			</view>
		</view>
		<view class="mine-tabBer-contaner">
			<tabBer></tabBer>
		</view>
	</view>
</template>

<script>
	import tabBer from "../../compenents/tabBer/tabBer.vue";
	import top from "../../compenents/top.vue"
	export default {
		data() {
			return {
				
			}
		},
		components: {
			tabBer,
			top
		},
		methods: {
			//设置跳转
			intercalateFun(){
				uni.navigateTo({
					url:"../intercalate/intercalate"
				})
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
	background-color: #f5f6fe;
}
.mine-view-container{
	flex-grow: 1;
	background-image: url(../../static/mine/backImg.png);
	background-size:750rpx 100%;
	background-repeat: no-repeat;
}
.mine-tabBer-contaner{
	padding: 20px 0 ;
}
.mine-container-information{
	text-align: right;
	margin-right: 20rpx;
}
.mine-index-information{
	width: 70rpx;
	height: 70rpx;
}
.mine-userLogo-container{
	text-align: center;
}
.mine-userLogo{
	width: 120rpx;
	height: 120rpx;
}
.mine-userInfo-container{
	text-align: center;
}
.mine-userInfo-name{
	font-size: 60rpx;
	color:#FFFFFF
}
.mine-userInfo-remaining{
	font-size: 35rpx;
	color:#FFFFFF
}
.mine-carte-flex{
	display: flex;
	flex-direction: column;
	justify-content: center;
	width: 750rpx;
	height: 65%;
}
.mine-carte-container{
	width: 750rpx;
	height: 140rpx;
	display: flex;
	justify-content:space-around;
	margin-top: 40rpx;
}
.mine-carte-conter{
	text-align: center;
}
.mine-carte-img{
	height: 80rpx;
}
.mine-carte-title{
	font-size: 30rpx;
	margin-top: 4rpx;
}



</style>
