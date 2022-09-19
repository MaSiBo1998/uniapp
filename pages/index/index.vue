<template>
	<view class="container">
		<van-swipe :autoplay="3000">
		  <van-swipe-item v-for="(image, index) in images" :key="index">
		    <img v-lazy="image" />
		  </van-swipe-item>
		</van-swipe>
	</view>
</template>

<script>
	
	export default {
		data() {
			return {
				images: [
				        'https://img01.yzcdn.cn/vant/apple-1.jpg',
				        'https://img01.yzcdn.cn/vant/apple-2.jpg',
				      ]
			}
		},
		methods: {

		}
	}
</script>

<style>
	.container {
		padding: 20px;
		font-size: 14px;
		line-height: 24px;
	}
</style>
