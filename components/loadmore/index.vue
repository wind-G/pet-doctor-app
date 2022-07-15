<template>
	<!-- loadmore -->
	<view class="loadmore">
		<text class="loadmore-text" v-if="loadmoreState === 'loadmore'">上拉加载更多</text>
		<text class="loadmore-text" v-else-if="loadmoreState === 'loading'">正在加载...</text>
		<text class="loadmore-text" v-else-if="loadmoreState === 'nomore'">没有更多了</text>
	</view>
</template>

<script>
  export default {
    name: 'loadmore',
		props: {
			loadmoreState:{
				type:String,
				default:true
			}
		},
    data() {
      return {

      }
    }
  }
</script>

<style>
	.loadmore {
		width: 100%;
		display: flex;
		justify-content: center;
		align-items: center;
		height: 72rpx;
	}
	.loadmore-text {
		font-size: 26rpx;
		font-weight: 700;
	}
</style>
