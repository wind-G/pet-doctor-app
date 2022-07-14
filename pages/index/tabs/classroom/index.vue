<template>
	<view class="clssroom">
		<Inset></Inset>
		<!-- type -->
		<view class="clssroom-header">
			<scroll-view class="room-header-type" :scroll-x="true" :show-scrollbar="true">
				<view :class="roomTypeIndex == 1?'room-type-ative':''" @click="roomTypeClick(1)">推荐</view>
				<view :class="roomTypeIndex == 2?'room-type-ative':''" @click="roomTypeClick(2)">饮食</view>
				<view :class="roomTypeIndex == 3?'room-type-ative':''" @click="roomTypeClick(3)">洗漱</view>
				<view :class="roomTypeIndex == 4?'room-type-ative':''" @click="roomTypeClick(4)">性格</view>
				<view :class="roomTypeIndex == 5?'room-type-ative':''" @click="roomTypeClick(5)">培养</view>
				<view :class="roomTypeIndex == 6?'room-type-ative':''" @click="roomTypeClick(6)">记录片</view>
				<view :class="roomTypeIndex == 7?'room-type-ative':''" @click="roomTypeClick(7)">文化</view>
				<view :class="roomTypeIndex == 8?'room-type-ative':''" @click="roomTypeClick(8)">搞笑</view>
			</scroll-view>
		</view>
		
		<!-- swiper -->
		<view class="room-swiper">
			<view class="room-swiper-content">
				<swiper class="room-carousel" :indicator-dots="false" autoplay :interval="3000" circular @change="change">
				  <swiper-item v-for="(item, index) in roomVideo" :key="index">
				    <view class="room-item">
							<image :src="item.image" class="room-image" mode=""></image>
							<view class="room-warp">
								<view class="room-warp-title">{{ item.title }}</view>
								<view class="room-warp-info">{{ item.info }}</view>
							</view>
				    </view>
				  </swiper-item>
				</swiper>
				<view class="dot-main">
					<view :class="['dot-item',current==index?'active':'']" v-for="(item,index) in roomVideo" :key="index"></view>
				</view>
			</view>
		</view>
		
		<!-- 最新推荐 -->
		<view class="room-new-box">
			<view class="room-new-video">
				<view class="block-title">
					<text class="block-text">最新推荐</text>
					<view class="block-link">更多<text class="iconfont icon-jiantouyou"></text></view>
				</view>
				<view class="room-new-warp">
					<view class="room-video-item" v-for="(item, index) in roomVideo" :key="index">
						<view class="room-video-img"><image class="r-video-img" :src="item.image" mode=""></image></view>
						<view class="room-video-wrap">
							<view class="r-video-title">{{ item.title }}</view>
							<view class="r-video-text">{{ item.info }}</view>
						</view>
					</view>
				</view>
			</view>
			<!-- loadmore -->
			<view class="loadmore">
			  <text class="loadmore-text" v-if="loadmoreState === 'loadmore'">上拉加载更多</text>
			  <text class="loadmore-text" v-else-if="loadmoreState === 'loading'">正在加载...</text>
			  <text class="loadmore-text" v-else-if="loadmoreState === 'nomore'">没有更多了</text>
			</view>
		</view>
		
		<bar-inset></bar-inset>
	</view>
</template>

<script>
	import Inset from "@/components/inset/index.vue"
	import BarInset from "@/components/bar-inset/index.vue"
	export default {
		components: {
			Inset,
			BarInset,
		},
		data() {
			return {
				roomTypeIndex: 1,
        /* swiper */
        roomVideo: [
					{
						"image" : "/static/images/img1.jpg",
						"title": "标题",
						"info": "这是一个内容"
					},
					{
						"image" : "/static/images/img2.jpg",
						"title": "标题22",
						"info": "这是一个内容222aaaaaaaaaaaaaaaaaa"
					},
					{
						"image" : "/static/images/img3.jpg",
						"title": "标题333",
						"info": "这是一个内容333"
					},
					{
						"image" : "/static/images/img4.jpg",
						"title": "标题444",
						"info": "这是一个内容444"
					},
					{
						"image" : "/static/images/img5.jpg",
						"title": "标题555",
						"info": "这是一个内容555"
					},
				],
				current: 0, // 指示点下标
        loadmoreState: 'loadmore',
			}
		},
		onLoad() {

		},
		methods: {
			// tab点击切换
			roomTypeClick(num){
				this.roomTypeIndex = num;
			},
			// 指示点切换
			change(e) {
				this.current = e.detail.current;
			}

		}
	}
</script>

<style lang="scss" scoped>
	.clssroom{
		width: 100%;
		display: block;
		.clssroom-header{
			width: 100%;
			display: block;
			padding: 20rpx 30rpx;
			box-sizing: border-box;
			background-color: #ffffff;
			// border-bottom: 1px solid #dddddd;
			.room-header-type{
				width: 100%;
				display: block;
				white-space: nowrap;
				overflow: hidden;
				overflow-x: auto;
				view{
					display: inline-block;
					vertical-align: middle;
					margin-right: 30rpx;
					font-size: 30rpx;
					color: #999999;
					position: relative;
				}
				.room-type-ative{
					font-size: 36rpx;
					font-weight: bold;
					color: #333333;
					position: relative;
					&::before{
						content: "";
						width: 30rpx;
						height: 6rpx;
						display: block;
						background-color: #24a7c5;
						border-radius: 50rpx;
						position: absolute;
						left: 0;
						right: 0;
						bottom: 0;
						z-index: 1;
						margin: auto;
					}
				}
			}
		}
	}
	.room-swiper{
		width: 100%;
		display: block;
		padding: 0rpx 30rpx;
		box-sizing: border-box;
		margin-top: 20rpx;
		.room-swiper-content{
			width: 100%;
			display: block;
			position: relative;
			.room-carousel{
				width: 100%;
				height: 350rpx;
				display: block;
				.room-item{
					border-radius: 20rpx;
					overflow: hidden;
					position: relative;
				}
				.room-item,
				.room-image{
					width: 100%;
					height: 100%;
					display: block;
				}
				.room-warp{
					width: 100%;
					display: block;
					padding: 0rpx 30rpx;
					box-sizing: border-box;
					position: absolute;
					left: 0;
					right: 0;
					bottom: 20rpx;
					z-index: 2;
					.room-warp-title{
						display: block;
						font-size: 32rpx;
						color: #ffffff;
					}
					.room-warp-info{
						font-size: 24rpx;
						color: #f2f2f2;
					}
				}
			}
			.dot-main{
				position: absolute;
				right: 20rpx;
				bottom: 20rpx;
				z-index: 1;
				display: flex;
				.dot-item{
					width: 10rpx;
					height: 10rpx;
					background-color: rgba(250, 250, 250, 0.3);
					border-radius: 0rpx;
					margin: 0rpx 5rpx;
					transition: 0.5s;
				}
				.active{
					width: 20rpx;
					background-color: #24a7c5;
					border-radius: 5rpx;
				}
			}
		}
	}
	.room-new-box{
		width: 100%;
		display: block;
		margin-top: 30rpx;
		.room-new-video{
			width: 100%;
			padding: 30rpx 30rpx;
			box-sizing: border-box;
			background-color: #ffffff;
			border-radius: 50rpx;
			.room-new-warp{
				width: 100%;
				display: flex;
				flex-wrap: wrap;
				justify-content: space-between;
				.room-video-item{
					width: 47%;
					display: inline-block;
					margin-top: 20rpx;
					.room-video-img{
						width: 100%;
						height: 260rpx;
						display: block;
						border-radius: 20rpx;
						overflow: hidden;
						.r-video-img{
							width: 100%;
							height: 100%;
							display: block;
						}
					}
					.room-video-wrap{
						width: 100%;
						display: block;
						margin-top: 15rpx;
						.r-video-title,
						.r-video-text{
							overflow: hidden;
							text-overflow: ellipsis;
							white-space: nowrap;
						}
						.r-video-title{
							display: block;
							font-size: 28rpx;
							color: #333333;
						}
						.r-video-text{
							font-size: 24rpx;
							color: #999999;
						}
					}
				}
			}
		}
	}
	.block-title{
		width: 100%;
		display: flex;
		align-items: center;
		position: relative;
		&::before{
			content: '';
			width: 6rpx;
			height: 36rpx;
			display: block;
			background-color: #24a7c5;
			border-radius: 5rpx;
			position: absolute;
			top: 0;
			left: 0;
			bottom: 0;
			margin: auto;
		}
		.block-text{
			flex: 1;
			display: block;
			font-size: 36rpx;
			color: #333333;
			font-weight: bold;
			padding-left: 20rpx;
			box-sizing: border-box;
		}
	}
	.block-link{
	  display: flex;
	  align-items: center;
		font-size: 26rpx;
		color: #999999;
		text{
			font-size: 26rpx;
		}
	}
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
