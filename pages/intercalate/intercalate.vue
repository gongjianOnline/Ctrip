<template>
	<view class="wrapper">
		<view class="intercalate-view-container">
			<topNavigation title="设置" leftIcon="../../static/topNavigation/left.png" />
			<view class="info-container">
				<view class="info-conter" @click="intercalateFun('userInfo')">
					<view class="info-conterLeft">
						<image src="../../static/mine/user_logo.png" alt="" class="infoLogo">
						<view class="info-title">个人主页</view>
					</view>
					<view class="info-conterRight">
						<span class="info-title">进入</span>
						<image src="../../static/mine/right.png" alt="" class="rightIcon">
					</view>
				</view>
				
				<view class="info-conter" @click="intercalateFun('card')">
					<view class="info-conterLeft">
						<image src="../../static/intercalate/bill.png" alt="" class="infoIcon">
						<view class="info-title">我的校园卡</view>
					</view>
					<view class="info-conterRight">
						<span class="info-title">2</span>
						<image src="../../static/mine/right.png" alt="" class="rightIcon">
					</view>
				</view>
				
				<view class="info-conter">
					<view class="info-conterLeft">
						<image src="../../static/intercalate/fixing.png" alt="" class="infoIcon">
						<view class="info-title">附近设备</view>
					</view>
					<view class="info-conterRight">
						<span class="info-title">3</span>
						<image src="../../static/mine/right.png" alt="" class="rightIcon">
					</view>
				</view>
				
				<view class="info-conter">
					<view class="info-conterLeft">
						<image src="../../static/intercalate/QRCode.png" alt="" class="infoIcon">
						<view class="info-title">我的二维码</view>
					</view>
					<view class="info-conterRight">
						<span class="info-title"></span>
						<image src="../../static/mine/right.png" alt="" class="rightIcon">
					</view>
				</view>
				
				<view class="info-conter">
					<view class="info-conterLeft">
						<image src="../../static/intercalate/collection.png" alt="" class="infoIcon">
						<view class="info-title">收藏</view>
					</view>
					<view class="info-conterRight">
						<span class="info-title"></span>
						<image src="../../static/mine/right.png" alt="" class="rightIcon">
					</view>
				</view>
				
				<view class="info-conter">
					<view class="info-conterLeft">
						<image src="../../static/intercalate/tidings.png" alt="" class="infoIcon">
						<view class="info-title">我的消息</view>
					</view>
					<view class="info-conterRight">
						<span class="info-title"></span>
						<image src="../../static/mine/right.png" alt="" class="rightIcon">
					</view>
				</view>
				
				<view class="info-conter">
					<view class="info-conterLeft">
						<image src="../../static/intercalate/customService.png" alt="" class="infoIcon">
						<view class="info-title">联系客服</view>
					</view>
					<view class="info-conterRight">
						<span class="info-title"></span>
						<image src="../../static/mine/right.png" alt="" class="rightIcon">
					</view>
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
			//路由跳转
			intercalateFun(name){
				uni.navigateTo({
					url:`../${name}/${name}`
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
	background: #FFFFFF;
}
.info-container{
	margin-top: 140upx;
	width: 750rpx;
	height: 750rpx;
}
.info-conter{
	width: 750rpx;
	height: 150rpx;
	box-shadow: 0px 0px 1px rgba(0,0,0,0.4);
	display: flex;
	align-items: center;
	justify-content:space-between;
	padding: 0 20rpx;
}
.info-conterLeft{
	display: flex;
	align-items: center;
}
.infoLogo{
	width: 120rpx;
	height: 120rpx;
}
.info-title{
	padding-left: 20rpx;
	font-size: 30rpx;
	font-weight: 500;
}
.info-conterRight{
	display: flex;
	align-items: center;
	
}
.rightIcon{
	width: 60rpx;
	height: 60rpx;
}
.infoIcon{
	width: 60rpx;
	height: 60rpx;
}
</style>
