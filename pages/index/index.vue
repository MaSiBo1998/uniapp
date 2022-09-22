<template>
	<view class="container">
		<van-grid square direction="horizontal" :column-num="2">
		  <van-grid-item v-for="value in 8" :key="value" icon="photo-o" text="文字" />
		</van-grid>
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
