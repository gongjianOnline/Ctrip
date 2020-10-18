<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
			 uni.hideTabBar({})
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		}
	}
</script>

<style lang="scss">
	@import "common/colorui/main.css";
	@import "common/colorui/icon.css";
	/*每个页面公共css */
	page {
	  height: 100%;
	}
	.uni-input-placeholder,.uni-input-input{
		padding-left: 10px;
	}

</style>
