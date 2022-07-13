<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		}
	}
</script>

<style>
	/*每个页面公共css */
	@import url("@/static/icon/iconfont.css");
	page {
		background-color: #f2f2f2;
	}
	/* #ifdef APP-PLUS */
	uni-swiper .uni-swiper-dot{
		width: 20rpx;
		height: 4rpx;
		background-color: #f2f2f2;
		border-radius: 0rpx;
	}
	uni-swiper .uni-swiper-dot-active{
		width: 40rpx;
		background-color: #24a7c5;
		border-radius: 5rpx;
	}
	/* #endif */
	
	/* #ifdef MP-WEIXIN */
	wx-swiper .wx-swiper-dot{
		width: 10rpx;
		height: 4rpx;
		background-color: #f2f2f2;
		border-radius: 0rpx;
	}
	wx-swiper .wx-swiper-dot-active{
		width: 40rpx;
		background-color: #24a7c5;
		border-radius: 5rpx;
	}
	/* #endif */
</style>
