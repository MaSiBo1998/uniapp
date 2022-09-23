<template>
	<view>
		<view class="type-top">
			<van-cell title="产品分类" icon="location-o" :border='false'>
			</van-cell>
			<view class="type">
				<van-grid :column-num="3" :border="false" :gutter='10'>
					<van-grid-item icon="photo-o" text="安装" v-if='type.indexOf(1)!== -1' />
					<van-grid-item icon="photo-o" text="维修" v-if='type.indexOf(2)!== -1' />
					<van-grid-item icon="photo-o" text="量尺" v-if='type.indexOf(3)!== -1' />
					<van-grid-item icon="photo-o" text="上门" v-if='type.indexOf(4)!== -1' />
					<van-grid-item icon="photo-o" text="文字" v-if='type.indexOf(5)!== -1' />
				</van-grid>
			</view>
		</view>
		<view class="type-form">
			<van-cell title="客户信息" icon="location-o" :border='false'>
			</van-cell>
		</view>
	</view>
</template>

<script>
	export default {
		props: ['type'],
		data() {
			return {

			}
		},
		methods: {

		},
		created() {
			console.log(this.type)
		}
	}
</script>

<style lang="scss">
	.type-top {
		background-color: #FFFFFF;
		margin-bottom: 5px;
	}
</style>
