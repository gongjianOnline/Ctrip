<template>
	<view class="qiun-columns">
		<view class="qiun-charts3">
			<canvas canvas-id="canvasArcbar1" id="canvasArcbar1" class="charts3"></canvas>
		</view>
	</view>
</template>

<script>
	import uCharts from '@/common/u-charts.min.js';
	var _self;
	var canvaArcbar1;

	export default {
		data() {
			return {
				cWidth3: '', //圆弧进度图
				cHeight3: '', //圆弧进度图
				arcbarWidth: '', //圆弧进度图，进度条宽度,此设置可使各端宽度一致
				pixelRatio: 1,
			}
		},
		created() {
			_self = this;
			this.cWidth3 = uni.upx2px(250); //这里要与样式的宽高对应
			this.cHeight3 = uni.upx2px(250); //这里要与样式的宽高对应
			this.arcbarWidth = uni.upx2px(24);
			this.getServerData();
		},
		methods: {
			getServerData() {
				let Arcbar1 = {
					series: [{
						name: '优秀',
						data: 0.95,
						color: '#000000'
					}]
				};
				_self.showArcbar("canvasArcbar1", Arcbar1);
			},
			showArcbar(canvasId, chartData) {
				console.log("调用了方法")
				console.log(chartData)
				canvaArcbar1 = new uCharts({
					$this: _self,
					canvasId: canvasId,
					type: 'arcbar',
					fontSize: 18,
					legend: {
						show: false
					},
					pixelRatio: _self.pixelRatio,
					series: chartData.series,
					animation: true,
					width:this.cWidth3 * 1.4,
					height: this.cHeight3 * 2,
					dataLabel: true,
					title: {
						name: Math.round(chartData.series[0].data * 100) + "%", //这里我自动计算了，您可以直接给任意字符串
						color: '#4b6288',
						fontSize: 26 * _self.pixelRatio
					},
					subtitle: {
						name: chartData.series[0].name, //这里您可以直接给任意字符串
						color: '#29334a',
						fontSize: 18
					},
					extra: {
						arcbar: {
							type: 'default',
							width: _self.arcbarWidth * _self.pixelRatio, //圆弧的宽度
							backgroundColor:"#ffffff"
						}
					}
				});

			}
		}
	}
</script>

<style>
	/*样式的width和height一定要与定义的cWidth和cHeight相对应*/
	.qiun-charts3 {
		width: 350upx;
		height: 350rpx;
	}
	.charts3 {
		width: 350upx;
		height: 200px;
	}
</style>
