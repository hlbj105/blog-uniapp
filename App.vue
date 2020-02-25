<script>
export default {
	onLaunch: function() {
		console.log('App Launch');
	},
	onShow: function() {
		console.log('App Show');
	},
	onHide: function() {
		console.log('App Hide');
	}
};
</script>

<style>
/* 解决头条小程序组件内引入字体不生效的问题 */
/* #ifdef MP-TOUTIAO */
@font-face {
	font-family: uniicons;
	src: url('/static/uni.ttf');
}
/* #endif */
view,text,image,swiper,swiper-item,scroll-view  {
	box-sizing: border-box;
}
page {
	background-color: #ededed;
}
</style>
<style lang="scss">
@import './static/css/iconfont.scss';
.more {
	line-height: 80rpx;
	text-align: center;
	color: $uni-text-color-grey;
}
</style>