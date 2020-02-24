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

		<uni-list>
			<uni-list-item :show-arrow="false" v-for="i in 5" :key="i">
				<navigator class="thumbnail" url="/pages/article/article">
					<image mode="aspectFill" src="https://cdn.huangliangbo.com/wp-content/uploads/2020/01/%E6%B7%B1%E5%BA%A6%E6%88%AA%E5%9B%BE_%E9%80%89%E6%8B%A9%E5%8C%BA%E5%9F%9F_20200117102417.png?imageView2/1/w/1304/h/926/interlace/1/q/100#"></image>
				</navigator>

				<view class="title">
					<view class="title-category">
						电脑&系统
					</view>
					<navigator url="/pages/article/article">
						360国产浏览器更新12.1.2000.0-1版本
					</navigator>
				</view>

				<view class="summary">
					内核终于从63升级到78了！ X86下载地址：链接: https://pan.baidu.com/s/1Ipum9C1bYHvXGdOybK-dbg 密码: 3qpa 其他版本下载去官网申请就可以
				</view>

				<view class="opeartion">
					<view>
						<text class="iconfont icon-date"></text>
						<text>2020-01-17 10:30:41</text>
					</view>
					<view>
						<text class="iconfont icon-hot1"></text>
						<text>217</text>
					</view>
					<view>
						<text class="iconfont icon-message"></text>
						<text>0</text>
					</view>
					<view>
						<text class="iconfont icon-good"></text>
						<text>2</text>
					</view>
				</view>
			</uni-list-item>
		</uni-list>
		
		<view class="more">
			加载中...
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
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

	.thumbnail {
		image {
			width: 100%;
			height: 300rpx;
			border-radius: 8rpx;
			transition: .5s;
		}
	}

	.title {
		margin: 30rpx 0;
		font-size: 32rpx;

		font-weight: 500;
		display: flex;
		align-items: center;

		.title-category {
			position: relative;
			margin-right: 20rpx;
			padding: 6rpx 10rpx;
			background-color: $uni-color-primary;
			border-radius: 6rpx;
			font-size: 24rpx;
			color: #fff;
			flex-shrink: 0;

			&::after {
				content: "";
				position: absolute;
				right: -20rpx;
				top: 50%;
				border: 10rpx solid transparent;
				border-left-color: $uni-color-primary;
				-webkit-transform: translateY(-50%);
				transform: translateY(-50%);
			}
		}

		navigator {
			overflow: hidden;
			text-overflow: ellipsis;
			white-space: nowrap;
		}
	}

	.summary {
		height: auto;
		display: -webkit-box;
		max-height: 151.2rpx;
		overflow: hidden;
		-webkit-box-orient: vertical;
		word-break: break-all;
		text-overflow: ellipsis;
		-webkit-line-clamp: 3;
		line-height: 1.6;
	}

	.opeartion {
		margin-top: 10px;
		font-size: 12px;
		color: #f2be45;
		display: flex;
		align-items: flex-end;
		width: 100%;
		margin-top: 10px;
		font-size: 12px;
		color: #f2be45;
		> view {
			display: flex;
			align-items: flex-end;
			margin-right: 20rpx;
			.iconfont {
				margin-right: 4rpx;
			}
		}
	}
</style>
