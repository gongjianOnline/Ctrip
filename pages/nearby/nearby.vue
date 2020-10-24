<template>
	<view>
		<topNavigation title="搜索附近设备" leftIcon="../../static/topNavigation/left.png" rightIcon="../../static/topNavigation/refresh.png" />
		<scroll-view :scroll-top="scrollTop" scroll-y="true" class="snearby-croll-Y">
			<view class="snearby-row-content" v-for="(item,index) in dataList" :key="index">
				<view class="snearby-row-info">
					<view class="snearby-row-maininfo">{{item.maininfo}}</view>
					<view class="snearby-row-secondaryinfo">{{item.secondaryinfo}}</view>
				</view>
				<view class="snearby-row-select">
					<view class="snearby-button" @click="skipFun">选择</view>
				</view>
			</view>
		</scroll-view>
		


	</view>
</template>

<script>
	import topNavigation from "@/compenents/topNavigation/topNavigation.vue";
	export default {
		data() {
			return {
				scrollTop:0,
				dataList:[
					{
						maininfo:'男生宿舍A栋',
						secondaryinfo:'男生宿舍6楼'
					},
					{
						maininfo:'男生宿舍A栋',
						secondaryinfo:'男生宿舍5楼'
					},
					{
						maininfo:'男生宿舍A栋',
						secondaryinfo:'男生宿舍4楼'
					},
					{
						maininfo:'男生宿舍A栋',
						secondaryinfo:'男生宿舍3楼'
					},
					{
						maininfo:'男生宿舍A栋',
						secondaryinfo:'男生宿舍2楼'
					},
					{
						maininfo:'男生宿舍A栋',
						secondaryinfo:'男生宿舍1楼'
					},
					{
						maininfo:'女生宿舍A栋',
						secondaryinfo:'女生宿舍6楼'
					},
					{
						maininfo:'女生宿舍A栋',
						secondaryinfo:'女生宿舍5楼'
					},
					{
						maininfo:'女生宿舍A栋',
						secondaryinfo:'女生宿舍4楼'
					},
					{
						maininfo:'女生宿舍A栋',
						secondaryinfo:'女生宿舍3楼'
					},
					{
						maininfo:'女生宿舍A栋',
						secondaryinfo:'女生宿舍2楼'
					},
					{
						maininfo:'女生宿舍A栋',
						secondaryinfo:'女生宿舍1楼'
					},
					
				]
			}
		},
		components: {
			topNavigation
		},
		methods: {
			skipFun(){
				uni.navigateTo({
					url:"../equipmentStatus/equipmentStatus",
					success:()=>{
					}
				})
			}
		}
	}
</script>

<style>
.snearby-croll-Y{
	margin-top: 100upx;
	height: 100%
}
.snearby-row-content{
	width: 750upx;
	height: 130upx;
	display: flex;
	justify-content: space-between;
	border-bottom: 1px solid rgba(157, 157, 157, 0.2);
}
.snearby-row-info{
	padding-left: 40upx;
	display: flex;
	flex-direction: column;
	justify-content: center;
}
.snearby-row-select{
	padding-right: 40upx;
	font-size: 35upx;
	display: flex;
	flex-direction: column;
	justify-content: center;
}
.snearby-row-maininfo{
	font-size: 35upx;
	color: #505050;
}
.snearby-row-secondaryinfo{
	font-size: 20upx;
	margin-top: 10upx;
	color: rgba(157, 157, 157, 1);
}
.snearby-button{
	padding: 10upx 30upx;
	border: 1px solid rgba(56, 56, 56, 1);
	border-radius: 10upx;
}

</style>
