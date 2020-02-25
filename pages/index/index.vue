<template>
	<view class="container">
		<swiper class="swiper" :indicator-dots="true" :autoplay="true" :interval="3000" :duration="1000">
			<swiper-item>
				<view class="swiper-item">
					<image src="https://cdn.huangliangbo.com/wp-content/uploads/2020/01/%E6%B7%B1%E5%BA%A6%E6%88%AA%E5%9B%BE_%E9%80%89%E6%8B%A9%E5%8C%BA%E5%9F%9F_20200117102417.png?imageView2/1/w/1304/h/926/interlace/1/q/100#"
					 mode="aspectFill"></image>
					<view class="swiper-text">
						360国产浏览器更新12.1.2000.0-1版本
					</view>
				</view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item">
					<image src="https://cdn.huangliangbo.com/wp-content/uploads/2019/12/1576337455-wxandios.png" mode="aspectFill"></image>
					<view class="swiper-text">
						360国产浏览器更新12.1.2000.0-1版本
					</view>
				</view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item">
					<image src="https://cdn.huangliangbo.com/wp-content/uploads/2020/01/%E6%B7%B1%E5%BA%A6%E6%88%AA%E5%9B%BE_%E9%80%89%E6%8B%A9%E5%8C%BA%E5%9F%9F_20200117102417.png?imageView2/1/w/1304/h/926/interlace/1/q/100#"
					 mode="aspectFill"></image>
					<view class="swiper-text">
						360国产浏览器更新12.1.2000.0-1版本360国产浏览器更新12.1.2000.0-1版本360国产浏览器更新12.1.2000.0-1版本360国产浏览器更新12.1.2000.0-1版本
					</view>
				</view>
			</swiper-item>
		</swiper>

		<postList />

		<uni-load-more :status="more"></uni-load-more>

	</view>
</template>

<script>
	import postList from '../../components/post-list/post-list.vue'
	export default {
		components: {
			postList
		},
		data() {
			return {
				more:'loading', // loading 的状态，可选值：more（loading前）、loading（loading中）、noMore（没有更多了）
				href: 'https://uniapp.dcloud.io/collocation/pages?id=easycom'
			}
		},
		methods: {

		}
	}
</script>

<style scoped lang="scss">
	.swiper {
		height: calc(100vw *3 / 4);
	}

	.swiper-item {
		image {
			width: 100%;
			height: calc(100vw *3 / 4);
		}

		view {
			position: absolute;
			bottom: 45rpx;
			width: 100%;
			height: 60rpx;
			line-height: 60rpx;
			background-color: rgba(0, 0, 0, .3);
			padding: 0 24rpx;
			color: #fff;
			overflow: hidden;
			text-overflow: ellipsis;
			white-space: nowrap;
		}
	}
</style>
