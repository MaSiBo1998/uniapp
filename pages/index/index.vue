<template>
	<view class="container">
		<van-grid square direction="horizontal" :column-num="2">
		  <van-grid-item icon="photo-o" text="文字" @click="toOrder([1,2,3])"/>
		  <van-grid-item icon="photo-o" text="文字" @click="toOrder([1,2])"/>
		  <van-grid-item icon="photo-o" text="文字" @click="toOrder([1,2,3])"/>
		  <van-grid-item icon="photo-o" text="文字" @click="toOrder([1,2,4])"/>
		  <van-grid-item icon="photo-o" text="文字" @click="toOrder([1,2,5])"/>
		  <van-grid-item icon="photo-o" text="文字" @click="toOrder([1,2,3])"/>
		  <van-grid-item icon="photo-o" text="文字" @click="toOrder([1,2,4])"/>
		  <van-grid-item icon="photo-o" text="文字" @click="toOrder([1,2,5])"/>
		  <van-grid-item icon="photo-o" text="文字" @click="toOrder([1,2])"/>
		  <van-grid-item icon="photo-o" text="文字" @click="toOrder([1,2])"/>
		  <van-grid-item icon="photo-o" text="文字" @click="toOrder([1,2,5])"/>
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
			toOrder(type){
				uni.navigateTo({
					url: '/pages/orderGoods/index',
					events:{
						putOrderType: function(type){
							return type
						}
					},
					success(res) {
						res.eventChannel.emit('putOrderType',type)
					}
				})
			}
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
