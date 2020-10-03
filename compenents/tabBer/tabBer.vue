<template>
	<view class="tabBer-wrapper">
		<view 	class="tabBer border-right-none"
				:class="[IsSelected=='首页'?'selected':'']"
				@click="selectedFun('首页')">首页</view>
		<view 	class="tabBer"
				:class="[IsSelected === '我的'?'selected':'']"
				@click="selectedFun('我的')">我的</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				IsSelected:"首页"
			}
		},
		methods: {
			selectedFun(name){
				this.IsSelected = name
			}
		}
	}
</script>

<style scoped>
.tabBer-wrapper{
	display: flex;
	justify-content: center;
	margin-bottom: 20px;
}
.tabBer{
	width: 150rpx;
	height: 30px;
	border: 1px solid rgb(126,134,236);
	border-radius: 8rpx;
	color: #007aff;
	text-align: center;
	line-height: 30px;
}
.border-right-none{
	border-right: none;
}
.selected{
	background-color: rgb(126,134,236);
	color:#FFFFFF;
}
</style>
