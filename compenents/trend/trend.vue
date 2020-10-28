<template>
	<view class="qiun-columns">
		<view class="qiun-charts">
			<canvas canvas-id="canvasLineA" id="canvasLineA" class="charts" @touchstart="touchLineA"></canvas>
		</view>
	</view>
</template>

<script>
	import uCharts from '@/common/u-charts.min.js';
	var _self;
	var canvaLineA = null;
	export default {
		data() {
			return {
				cWidth: '',
				cHeight: '',
				pixelRatio: 1,
			}
		},
		created() {
			_self = this;
			this.cWidth = uni.upx2px(750);
			this.cHeight = uni.upx2px(400);
			this.getServerData();
		},
		methods: {
			getServerData() {
				console.log("调用了走势图")
				let LineA = {
					categories: ['9:30', '10:00', '10:30', '11:00', '11:30', '12:00'],
					series: [{
						name: '变化趋势',
						data: [80, 75, 80, 82, 85, 86],
						color: '#000000'
					}]
				};
				_self.showLineA("canvasLineA", LineA);
			},
			showLineA(canvasId, chartData) {
				canvaLineA = new uCharts({
					$this: _self,
					canvasId: canvasId,
					type: 'line',
					fontSize: 11,
					legend: {
						show: true
					},
					dataLabel: false,
					dataPointShape: true,
					background: '#FFFFFF',
					pixelRatio: _self.pixelRatio,
					categories: chartData.categories,
					series: chartData.series,
					animation: true,
					xAxis: {
						type: 'grid',
						gridColor: '#CCCCCC',
						gridType: 'dash',
						dashLength: 8
					},
					yAxis: {
						gridType: 'dash',
						gridColor: '#CCCCCC',
						dashLength: 8,
						splitNumber: 5,
						min: 20,
						max: 100,
						format: (val) => {
							return val.toFixed(0)
						}
					},
					width: _self.cWidth * _self.pixelRatio,
					height: this.cHeight ,
					extra: {
						line: {
							type: 'straight'
						}
					}
				});

			}
		}
	}
</script>

<style scoped>
	/*样式的width和height一定要与定义的cWidth和cHeight相对应*/
	.qiun-charts {
		width: 750upx;
		height: 400upx;
	}

	.charts {
		width: 750upx;
		height: 400upx;
		background-color: #FFFFFF;
	}
</style>
