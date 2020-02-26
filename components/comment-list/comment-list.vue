<template>
	<uni-list>
		<uni-list-item :show-arrow="false" v-for="i in 5" :key="i">
			<view class="comment-list">
				<image src="https://cdn.v2ex.com/gravatar/61d0dc88ed6970dd0e44d1bf5b60a20b?s=96&amp;r=g" width="60" height="60" alt=""
				 class="list-gravatar">
					<view class="list-header">
						<text class="author">黄良钵</text>
						<text class="icon-vip icon-level vip-style-1 vip1"></text>
						<view class="inline-block system-wrap">
							<text class="browser-info undefined"></text>
							<text class="system-info"></text>
						</view>
					</view>
					<view class="list-content">
						<view>@<text class="c-theme">xiaomo</text> 这东西也不难，了解过，就顺便试下</view>
					</view>
					<view class="list-footer">
						<text>2019-09-11 14:35:46</text>
						<view class="opinion">
							<view class="opinion-btn">
								<text class="iconfont icon-good"></text>
								0
							</view>
							<view class="opinion-btn"><text class="iconfont icon-bad"></text>
								0
							</view>
						</view>
					</view>
			</view>
		</uni-list-item>
	</uni-list>
</template>

<script>
</script>

<style lang="scss" src="./comment-list.scss"></style>
