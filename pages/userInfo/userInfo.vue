<template>
	<view class="wrapper">
		<view class="userInfo-view-container">
			<topNavigation title="个人信息" leftIcon="../../static/topNavigation/left.png" />
			<view class="userInfo-view-header">
				<view class="logo-container">
					<image src="../../static/login/logo.png" alt="" class="logoIcon">
					<span class="logoIcon-title">健康饮水</span>
				</view>
				<view class="logoUser-container">
					<image src="../../static/mine/user_logo.png" alt="" class="userLogo">
				</view>
			</view>
		</view>
		<view class="userInfo-containers">
			<view class="userInfo-title">admin</view>
			<view class="userinfo-details">卡内余额: 93.65元</view>
		</view>
		<view class="userInfo-carte-container">
			<view class="userInfo-carte-Item">
				<view class="userInfo-sculpture">
					<view class="userInfoIcon">
						<image src="../../static/userInfo/account.png" alt="" class="meunIcon">
					</view>
					<view class="userInfoIcon-info">292876034</view>
				</view>
				<view class="userInfoIcon-right">
					<!-- <image src="../../static/mine/right.png" alt="" class="userInfoIcon-rightIcon"> -->
				</view>
			</view>
			<view class="userInfo-carte-Item">
				<view class="userInfo-sculpture">
					<view class="userInfoIcon">
						<image src="../../static/userInfo/info.png" alt="" class="meunIcon">
					</view>
					<view class="userInfoIcon-info">男 22岁 水瓶座 山西-大同</view>
				</view>
				<view class="userInfoIcon-right">
					<image src="../../static/mine/right.png" alt="" class="userInfoIcon-rightIcon">
				</view>
			</view>
			<view class="userInfo-carte-Item">
				<view class="userInfo-sculpture">
					<view class="userInfoIcon">
						<image src="../../static/userInfo/school.png" alt="" class="meunIcon">
					</view>
					<view class="userInfoIcon-info">廊坊职业技术学院 15数字媒体1班</view>
				</view>
				<view class="userInfoIcon-right">
					<!-- <image src="../../static/mine/right.png" alt="" class="userInfoIcon-rightIcon"> -->
				</view>
			</view>
			<view class="userInfo-carte-Item">
				<view class="userInfo-sculpture">
					<view class="userInfoIcon">
						<image src="../../static/userInfo/charts.png" alt="" class="meunIcon">
					</view>
					<view class="userInfoIcon-info">打水记录</view>
				</view>
				<view class="userInfoIcon-right">
					<image src="../../static/mine/right.png" alt="" class="userInfoIcon-rightIcon">
				</view>
			</view>
			<view class="userInfo-carte-Item">
				<view class="userInfo-sculpture">
					<view class="userInfoIcon">
						<image src="../../static/userInfo/play.png" alt="" class="meunIcon">
					</view>
					<view class="userInfoIcon-info">支付方式绑定</view>
				</view>
				<view class="userInfoIcon-right">
					<image src="../../static/mine/right.png" alt="" class="userInfoIcon-rightIcon">
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

<style scoped>
.wrapper{
	display: flex;
	flex-direction: column;
	width: 750rpx;
	background: #FFFFFF;
}
.userInfo-view-container{
	margin-top: 100rpx;
	width: 750rpx;
	height: 100%;
}
.userInfo-view-header{
	width: 750rpx;
	height: 400rpx;
	background: linear-gradient(130deg, rgba(166,196,252,1) 26%, rgba(206,195,252,1) 100%);
	display: flex;
	justify-content: center;
	align-items: center;
	position: relative;
}
.logo-container{
	width: 750rpx;
	height: 200rpx;
	display: flex;
	justify-content: center;
	align-items: center;
}
.logoIcon{
	height: 150rpx;
	width: 120rpx;
}
.logoIcon-title{
	font-size: 60rpx;
	letter-spacing:20rpx;
	padding-left: 20rpx;
	color: #ffffff;
}
.logoUser-container{
	position: absolute;
	bottom: -100rpx;
	left: 50%;
	width: 200rpx;
	height: 200rpx;
	transform: translateX(-50%);
}
.userLogo{
	width: 100%;
	height: 100%;
}
.userInfo-containers{
	width: 750rpx;
	margin-top: 110rpx;
}
.userInfo-title{
	text-align: center;
	font-size: 40rpx;
}
.userinfo-details{
	text-align: center;
	font-size: 20rpx;
	color:#7d3232;
}
.userInfo-carte-container{
	width: 750rpx;
	height: 500rpx;
	margin-top: 30rpx;
}
.userInfo-carte-Item{
	width: 750rpx;
	height: 96rpx;
	padding: 0 20rpx;
	display: flex;
	justify-content: space-between;
	align-items: center;
	box-shadow: 0px 1px 1px -1px rgba(0,0,0,0.4);
}
.userInfo-sculpture{
	display: flex;
	align-items: center;
}
.userInfoIcon{
	width: 60rpx;
	height: 55rpx;
	display: flex;
	justify-content: center;
	align-items: center;
}
.userInfoIcon-info{
	padding-left: 20rpx;
	font-size: 30rpx;
}
.userInfoIcon-right{
	width: 100rpx;
	height: 100rpx;
	display: flex;
	justify-content: center;
	align-items: center
}
.userInfoIcon-rightIcon{
	width: 60rpx;
	height:60rpx;
}
.meunIcon{
	width: 100%;
	height: 100%;
}

</style>
