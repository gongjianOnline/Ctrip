<template>
	<view class="wrapper">
		<view class="view-container">
			
		</view>
		<tabBer class="tabber"></tabBer>
	</view>
</template>

<script>
	import tabBer from "../../compenents/tabBer/tabBer.vue"
	export default {
		data() {
			return {
				
			}
		},
		components: {
			tabBer
		},
		methods: {
			
		}
	}
</script>

<style scoped>
.wrapper{
	display: flex;
	flex-direction: column;
}
.view-container{
	flex-grow:1;
	border: 1px solid red;
}
.tabber{
	/* flex-grow:1; */
}
</style>
