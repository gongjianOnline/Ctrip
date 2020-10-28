<template>
	<view class='card-wrapper'>
		<view class="card-view-container">
			<topNavigation title="设备状态" leftIcon="../../static/topNavigation/left.png" />
			<view class="cardImg-contanier">
				<image src="img" alt="" class="cardImg">
			</view>
			<view class="cardInfo-container">
				<view class="cardInfo-left">
					<view class="cardInfo-leftImg">
						<image src="../../static/mine/user_logo.png" alt="" class="leftImg">
					</view>
					<view class="cardInfo-leftInfo">
						<view>
							<view class="cardInfo-leftInfoTitle">校园卡</view>
							<view class="cardInfo-leftInfoType">饭卡\水卡</view>
						</view>
						<view class="cardInfo-leftInfoCode">
							*** *** *** *034
						</view>
					</view>
				</view>
				<view class="cardInfo-right">
					<view class="cardInfo-statec">使用中</view>
				</view>
			</view>
			<view class="cardInfo-container">
				<view class="cardInfo-left">
					<view class="cardInfo-leftImg">
						<image src="../../static/mine/user_logo.png" alt="" class="leftImg">
					</view>
					<view class="cardInfo-leftInfo">
						<view>
							<view class="cardInfo-leftInfoTitle">校园卡</view>
							<view class="cardInfo-leftInfoType">饭卡\水卡</view>
						</view>
						<view class="cardInfo-leftInfoCode">
							*** *** *** *034
						</view>
					</view>
				</view>
				<view class="cardInfo-right">
					<view class="cardInfo-statec cardInfo-statec-cancel">已挂失</view>
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
	.card-wrapper {
		display: flex;
		flex-direction: column;
		width: 750rpx;
		height: 100%;
		background:#f5f6fe;
	}

	.card-view-container {
		flex-grow: 1;
		background-image: url(../../static/mine/backImg.png);
		background-size: 750rpx;
		background-repeat: no-repeat;
	}
	.cardImg-contanier{
		margin-top: 100rpx;
		margin-bottom: 100rpx;
		width: 750rpx;
		height: 400rpx;
		display: flex;
		justify-content: center;
		align-items: center;
	}
	.cardImg{
		height: 200rpx;
	}
	.cardInfo-container{
		width: 750rpx;
		display: flex;
		justify-content:space-between;
		padding:20rpx 10rpx;
		background: #fff;
		margin-bottom: 10rpx;
		border-radius: 10rpx;
		box-shadow: 0px 2px 2px -1px rgba(0,0,0,0.1);
	}
	.cardInfo-left{
		display: flex;
	}
	.cardInfo-leftImg{
		width: 150rpx;
		height: 150rpx;
		text-align: center;
		line-height: 150rpx;
	}
	.leftImg{
		width: 140rpx;
		height: 140rpx;
	}
	.cardInfo-leftInfo{
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		margin-left: 20rpx;
	}
	.cardInfo-leftInfoTitle{
		font-size: 34rpx;
		margin-bottom: 10rpx;
	}
	.cardInfo-leftInfoType{
		font-size: 24rpx;
	}
	.cardInfo-leftInfoCode{
		font-size: 34rpx;
	}
	.cardInfo-right{
	}
	.cardInfo-statec{
		padding:10rpx 20rpx;
		background: #899ff3;
		color: #ffffff;
		border-radius: 10rpx;
	}
	.cardInfo-statec-cancel{
		background-color:#ccc
	}
</style>
