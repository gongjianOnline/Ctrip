<template>
	<view class="wrapper">
		<image src="../../static/login/bgImg.png" mode="" class="bgimg"></image>
		<image src="../../static/login/logo.png" mode="" class="logo"></image>
		<view class="" class="title">健康饮水</view>
		<view class="form-wrapper">
			<view class="form-tiem">
				<view class="form-tiem-title">
					<image src="../../static/login/phone.png" mode=""></image>
				</view>
				<view class="form-tiem-input">
					<input class="uni-input" focus placeholder="电话" />
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	import top from "../../compenents/top.vue" 
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		components:{
			top
		},
		onLoad() {
			uni.hideTabBar()
		},
		methods: {

		}
	}
</script>

<style>
	.wrapper{
		width: 750rpx;
		height: 100%;
		background: #f5f6fe;
		position: relative;
		
	}
	.bgimg{
		width: 750rpx;
		height: 90%;
	}
	.logo{
		position: absolute;
		left: 40%;
		top: 5%;
		width: 150rpx;
		height: 150rpx;
	}
	.title{
		color: #FFFFFF;
		position: absolute;
		left: 30%;
		top:18%;
		font-size:80rpx;
		font-weight: bold;
	}
	.form-wrapper{
		position: absolute;
		left: 0px;
		bottom: 10%;
		width: 750rpx;
		height: 300px;
		border: 1px solid red;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}
	.form-tiem{
		display: flex;
	}
	.form-tiem-title{
		display: flex;
		justify-content: center;
		align-items: center;
	}
	.form-tiem-title>image{
		width: 60px;
		height: 60px;
	}
	.form-tiem-input{
		display: flex;
		justify-content: center;
		align-items: center;
	}
	.form-tiem-input>input{
		border: 1px solid red;
		border-radius: 90rpx;
		height: 40px;
		
	}
</style>
