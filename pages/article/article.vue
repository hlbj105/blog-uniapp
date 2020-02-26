<template>
	<view>
		<view class="section main">

			<view class="title">
				Python的switch替换方案、列表推导式、字典推导式
			</view>

			<view class="info">
				<view class="info-col">
					<view class="info-col-span">
						<text class="iconfont icon-about"></text>
						<text>黄良钵</text>
					</view>
					<view class="info-col-span info-time">
						<text class="iconfont icon-date"></text>
						<text>2020-2-26 09:48:41</text>
					</view>
				</view>
				<view class="info-col">
					<view class="info-col-span">
						<text>分类：</text>
						<text>程序开发</text>
					</view>
					<view class="info-col-span">
						<text class="iconfont icon-hot1"></text>
						<text>14</text>
					</view>
					<view class="info-col-span">
						<text class="iconfont icon-message-f"></text>
						<text>0</text>
					</view>
				</view>
			</view>

			<!-- 正文 -->
			<view class="content">
				<parser :html="html" />
			</view>

		</view>

		<!-- 评价 -->
		<view class="section operation">
			<!-- 评价 -->
			<view class="opinion">
				<view class="list">
					<view class="total">
						<text class="iconfont icon-loading" style="display: none;"></text> 1人
					</view>
					<image src="/static/image/like_love.png" mode="widthFix">
						<view class="block">Love</view>
				</view>
				<view class="list">
					<view class="total"><text class="iconfont icon-loading" style="display: none;"></text> 0人
					</view>
					<image src="/static/image/like_haha.png" mode="widthFix">
						<view class="block">Haha</view>
				</view>
				<view class="list">
					<view class="total"><text class="iconfont icon-loading" style="display: none;"></text> 0人
					</view>
					<image src="/static/image/like_wow.png" mode="widthFix">
						<view class="block">Wow</view>
				</view>
				<view class="list">
					<view class="total"><text class="iconfont icon-loading" style="display: none;"></text> 0人
					</view>
					<image src="/static/image/like_sad.png" mode="widthFix">
						<view class="block">Sad</view>
				</view>
				<view class="list">
					<view class="total"><text class="iconfont icon-loading" style="display: none;"></text> 0人
					</view>
					<image src="/static/image/like_angry.png" mode="widthFix">
						<view class="block">Angry</view>
				</view>
			</view>

			<!-- 标签 -->
			<view class="tag-wrap">
				<text class="iconfont icon-tag"></text>
				<text>Python、</text>
				<text>switch、</text>
				<text>列表推导式、</text>
				<text>字典推导式</text>
			</view>

			<!-- 上下篇 -->
			<view class="relative-link-wrap">
				<view class="prev">
					<view v-if="0">已是第一篇文章！</view>
					<view>
						<text>上一篇：</text>
						<navigator url="" class="">Vue History模式下微信支付授权目录的填写,处理URL未注册</navigator>
					</view>
				</view>
				<view class="next">
					<view v-if="0">已是最后一篇文章！</view>
					<view>
						<text>下一篇：</text>
						<navigator url="/2207" class="">Vue History模式下微信支付授权目录的填写,处理URL未注册</navigator>
					</view>
				</view>
			</view>

		</view>

		<!-- 评论区 -->
		<view class="section comment">
			<view class="comment-title">
				共 5 条评论
			</view>

			<commentList />
		</view>
			<uni-load-more :status="more"></uni-load-more>
	</view>
</template>

<script>
	import parser from '../../components/jyf-parser/jyf-parser.vue'
	import commentList from '../../components/comment-list/comment-list.vue'
	export default {
		components: {
			parser,
			commentList
		},
		data() {
			return {
				more: 'loading', // loading 的状态，可选值：more（loading前）、loading（loading中）、noMore（没有更多了）
				html: '<style>.a{font-style:italic}#b{font-weight:bold}p{text-align:center}</style>' +
					'<p><view class="a">Hello </view><view id="b">World!</view></p>'
			}
		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.section {
		margin: 24rpx;
		background-color: #FFFFFF;
		border-radius: 8rpx;
		padding: 30rpx;
	}

	.main {

		.title {
			padding: 20rpx 0;
			font-size: 40rpx;
			font-weight: 500;
			color: #666666;
		}

		.info {
			display: flex;
			flex-wrap: wrap;
			justify-content: center;
			align-items: center;
			margin-bottom: 20rpx;
			padding-bottom: 10rpx;
			border-bottom: 1rpx solid #e9eaed;
			text-align: center;
			color: #999;
			font-size: 28rpx;

			.info-col {
				margin-top: 8rpx;
				flex-shrink: 0;
				display: flex;
				align-items: center;

				.info-col-span {
					margin-left: 10rpx;
				}
			}
		}

		.content {
			line-height: 2;
			word-break: break-all;
		}
	}

	.operation {
		color: #666666;

		.opinion {
			display: flex;
			justify-content: center;
			margin-bottom: 40rpx;
			text-align: center;
			justify-content: space-between;

			.list {
				width: 100rpx;
				color: #666666;

				.total {
					font-size: 24rpx;
				}

				image {
					width: 80rpx;
					height: 80rpx;
					vertical-align: top;
					border: 0;
				}
			}
		}

		.tag-wrap {
			margin-bottom: 40rpx;
			text-align: center;
		}

		.relative-link-wrap {

			.prev,
			.next {
				>view {
					display: flex;
					text {
						flex-shrink: 0;
					}
				}
			}

			.next {
				margin-top: 20rpx;
			}
		}
	}
	
	.comment {
		padding: 0;
		.comment-title {
			padding: 30rpx; 
		}
	}
</style>
