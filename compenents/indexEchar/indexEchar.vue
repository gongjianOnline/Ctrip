<template>
	<view class="qiun-columns">
		<view class="qiun-charts">
			<canvas canvas-id="canvasPie" id="canvasPie" class="charts"></canvas>
		</view>
	</view>
</template>
<script>
	import uCharts from '@/common/u-charts.min.js';
	var _self;
	var canvaPie = null;
	export default {
		data() {
			return {
				cWidth: '',
				cHeight: '',
				pixelRatio: 1,
				serverData: '',
			}
		},
		mounted() {
			_self = this;
			this.cWidth = uni.upx2px(750);
			this.cHeight = uni.upx2px(500);
			this.getServerData();
			console.log(this.cWidth);
			console.log(this.cHeight)
			
		},
		methods: {
			getServerData() {
				console.log("调用了他")
				let chartData = {
					series: [{
						"name": "一班",
						"data": 50
					}, {
						"name": "二班",
						"data": 30
					}, {
						"name": "三班",
						"data": 20
					}, {
						"name": "四班",
						"data": 18
					}, {
						"name": "五班",
						"data": 8
					}]
				}
				_self.showPie("canvasPie", chartData);
			},
			showPie(canvasId, chartData) {
				console.log("方法被掉了")
				canvaPie = new uCharts({
					$this: _self,
					canvasId: canvasId,
					type: 'pie',
					fontSize: 11,
					legend: {
						show: true
					},
					pixelRatio: _self.pixelRatio,
					series: chartData.series,
					animation: true,
					width: 320,
					height: 200,
					dataLabel: true,
					extra: {
						pie: {
							lableWidth: 15
						}
					},
				});
				console.log("123456")
				console.log(canvaPie)
			}
		}
	}
</script>
<style>
	.charts {
		width: 750upx;
		height: 500upx;
	}
</style>
