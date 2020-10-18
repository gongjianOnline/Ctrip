<template>
	<view class="topNavigation-wrapper">
		<div class="topNavigation-imag-content" @click="backFun">
			<image :src="leftIcon" mode="" class="topNavigation-imageIcon"></image>
		</div>
		<div class="topNavigation-title topNavigation-imag-content">{{title}}</div>
		<div class="topNavigation-imag-content" @click="rightFun">
			<image :src="rightIcon" mode="" class="topNavigation-imageIcon"></image>
		</div>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		props:{
			title:{
				type:String,
				default:''
			},
			leftIcon:{
				type:String,
				default:""
			},
			rightIcon:{
				type:String,
				default:""
			},
			routerName:{
				type:String,
				default:""
			}
			
		},
		methods: {
			backFun(){
				uni.navigateBack({
				    delta: 1
				});
			},
			rightFun(){
				console.log("刷新")
			}
			
		}
	}
</script>

<style scoped>
.topNavigation-wrapper{
	width: 750upx;
	height: 100upx;
	background: linear-gradient(0.45turn, #9BA1F4, #63dcea);
	display: flex;
	justify-content: space-between;
	position: fixed;
	left: 0px;
	top: 0px;
	z-index: 1;
}
.topNavigation-imag-content{
	display: flex;
	justify-content: center;
	align-items: center;
}
.topNavigation-imageIcon{
	height: 60upx;
	width: 60upx;
	padding: 0 10upx;
}
.topNavigation-title{
	color: #FFFFFF;
	font-size: 40upx;
}


</style>
