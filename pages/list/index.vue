<template>
	<view >
		接单大厅
		<van-button type="warning" @click="toUserPage">警告按钮</van-button>
	</view>
</template>

<script>
	export default {
		data() {
			
		},
		methods: {
			toUserPage() {
				uni.navigateTo({
					url: '/pages/call/index'
				})
				return
			}
		},
	}
</script>

<style>
</style>