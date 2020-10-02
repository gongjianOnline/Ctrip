<template>
	<view class="wrapper">
		<view class="tabBer">首页</view>
		<view class="tabBer">我的</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style scoped>
.wrapper{
	display: flex;
	justify-content: center;
	border: 1px solid red;
}
.tabBer{
	width: 150rpx;
	height: 30px;
	border: 1px solid #007AFF;
	text-align: center;
	line-height: 30px;
	
}
</style>
