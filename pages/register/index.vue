<template>
	<view class="wrapper">
		<image src="../../static/login/bgImg.png" mode="" class="bgimg"></image>
		<image src="../../static/login/logo.png" mode="" class="logo"></image>
		<view class="" class="title">健康饮水</view>
		<view class="form-wrapper">s
			<view class="form-tiem">
				<view class="form-tiem-title">
					<image src="../../static/login/me.png" mode=""></image>
				</view>
				<view class="form-tiem-input">
					<input class="uni-input" focus placeholder="电话" v-model="phone"/>
				</view>
			</view>
			<view class="form-tiem">
				<view class="form-tiem-title">
					<image src="../../static/login/phone.png" mode=""></image>
				</view>
				<view class="form-tiem-input">
					<input class="uni-input" focus placeholder="电话" v-model="phone"/>
				</view>
			</view>
			<view class="form-tiem">
				<view class="form-tiem-title">
					<image src="../../static/login/password.png" mode=""></image>
				</view>
				<view class="form-tiem-input">
					<input class="uni-input" focus placeholder="密码" v-model="paswrod"/>
				</view>
			</view>
			<view class="button-container">
				<view class="button" @click="loginFun">
					注册
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
				title: '',
				phone:"",
				paswrod:""
			}
		},
		components:{
			top
		},
		onLoad() {
			uni.hideTabBar()
		},
		methods: {
			registeFun(){
				console.log("注册账号")
			},
			loginFun(){
				console.log("登录事件")
			}
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
		height: 190rpx;
	}
	.title{
		color: #FFFFFF;
		position: absolute;
		left: 30%;
		top:20%;
		font-size:80rpx;
		font-weight:400;
	}
	.form-wrapper{
		position: absolute;
		left: 0px;
		bottom: 10%;
		width: 750rpx;
		height: 300px;
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
		/* border: 1px solid #2C405A; */
	}
	.form-tiem-title>image{
		width: 60px;
		height: 60px;
	}
	.form-tiem-input{
		/* border: 1px solid #2C405A; */
		display: flex;
		justify-content: center;
		align-items: flex-start;
	}
	.form-tiem-input>input{
		border-width:1px;
		border-style: solid;
		border-image: linear-gradient(to left, #63dcea, #9BA1F4) 20 20;
		height: 46px;
		width: 450rpx;
	}
	.button-container{
		margin-top: 10px;
	}
	.button{
		width: 450rpx;
		height: 40px;
		text-align: center;
		line-height: 40px;
		background: linear-gradient(0.25turn, #9BA1F4, #63dcea);
		border-radius: 40rpx;
		color: #FFFFFF;
	}
	
</style>
