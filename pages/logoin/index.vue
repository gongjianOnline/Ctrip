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
					<input class="uni-input" type="text" focus placeholder="电话" @confirm="getPhone"	/>
				</view>
			</view>
			<view class="form-tiem">
				<view class="form-tiem-title">
					<image src="../../static/login/password.png" mode=""></image>
				</view>
				<view class="form-tiem-input">
					<input class="uni-input" password type="text" placeholder="密码" v-model="paswrod" @confirm="getPaswrod"/>
				</view>
			</view>
			<view class="register" @click="registeFun">注册账号</view>
			<view class="button-container">
				<view class="button" @click="loginFun">
					登录
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
				title: 'Hello',
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
			getPhone(event){
				this.phone = event.target.value
				uni.hideKeyboard();
			},
			getPaswrod(){
				uni.hideKeyboard();
			},
			registeFun(){
				console.log("999")
				uni.navigateTo({
				    url: "../register/index",
				    success: res => {},
				    fail: () => {},
				    complete: () => {}
				});
			},
			loginFun(){
				if(this.phone === "admin" && this.paswrod === "admin"){
					uni.reLaunch({
					    url: "../view/index",
					    success: res => {},
					    fail: () => {},
					    complete: () => {}
					});
				}
				
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
	.register{
		text-align: right;
		width: 750rpx;
		margin-right: 20px;
		color: #89a5f8;
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
