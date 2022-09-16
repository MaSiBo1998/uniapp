<template>
	<view >
		我的订单
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
					url: '/pages/user/index'
				})
				return
			}
		},
	}
</script>

<style>
</style>