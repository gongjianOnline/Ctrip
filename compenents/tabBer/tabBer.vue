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
		mounted(){
			uni.getStorage({
			    key: 'tabBerIndex',
			    success:(res)=>{
			        this.IsSelected = res.data?res.data:"首页"
			    }
			});
		},
		methods: {
			selectedFun(name){
				uni.setStorage({
				    key: 'tabBerIndex',
				    data: name,
				});
				this.IsSelected = name;
				let router = "";
				if(name === "首页"){
					router = "view"
				}else{
					router = "mine"
				}
				uni.reLaunch({
				    url: `../${router}/${router}`,
				    success: res => {},
				    fail: () => {},
				    complete: () => {}
				});
				
			}
		}
	}
</script>

<style scoped>
.tabBer-wrapper{
	display: flex;
	justify-content: center;
	padding:40upx 0;
	background:transparent;
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
