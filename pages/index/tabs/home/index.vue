<template>
	<view class="home">
		<view class="home-header">
			<!-- 轮播 -->
			<swiper class="carousel" indicator-dots autoplay :interval="3000" circular>
			  <swiper-item v-for="(item, index) in carousels" :key="index">
			    <view class="carousel-item">
						<image :src="item.image" class="carousel-image" mode="" @click="imageclick(item)"></image>
						<!-- <image class="carousel-image" src="@/static/images/1.jpg" mode=""></image> -->
			    </view>
			  </swiper-item>
			</swiper>
			
			<!-- 搜索 -->
			<view class="home-search">
				<view class="home-search-box">
					<view class="home-search-icon">
						<view class="iconfont icon-fujinjihuo"></view>
						<view class="home-icon-text">重庆</view>
					</view>
					<view class="home-search-center">
						<view class="home-search-wrap">
							<view class="iconfont icon-sousuo2"></view>
							<view class="home-search-text">搜索附近宠物医院</view>	
						</view>	
						<view class="home-search-button">
							搜索
						</view>
					</view>
				</view>
			</view>	
		</view>
		
		<!-- type -->
		<view class="home-type-block home-top">
			<view class="home-block">
				<view class="block-title"><text class="block-text">热门推荐</text></view>
				<view class="home-type">
					<scroll-view class="column-scroll-view" :scroll-x="true" :show-scrollbar="true">
						<view class="type-item">
							<image class="type-img" src="/static/images/1.jpg"></image>
							<text class="type-text">宠物领养</text>
						</view>
						<view class="type-item">
							<image class="type-img" src="/static/images/1.jpg"></image>
							<text class="type-text">宠物体检</text>
						</view>
						<view class="type-item">
							<image class="type-img" src="/static/images/1.jpg"></image>
							<text class="type-text">疫苗服务</text>
						</view>
						<view class="type-item">
							<image class="type-img" src="/static/images/1.jpg"></image>
							<text class="type-text">寄养照顾</text>
						</view>
						<view class="type-item">
							<image class="type-img" src="/static/images/1.jpg"></image>
							<text class="type-text">购买用品</text>
						</view>
					</scroll-view>
				</view>
			</view>
		</view>
		
		<!-- 讲堂 -->
		<view class="home-video-block home-top">
			<view class="home-video">
				<view class="block-title">
					<text class="block-text">热门讲堂</text>
					<view class="block-link">更多<text class="iconfont icon-jiantouyou"></text></view>
				</view>
				<view class="home-video-content">
					<scroll-view class="column-scroll-view" :scroll-x="true" :show-scrollbar="true">
						<view class="home-video-item">
							<image class="video-img" src="/static/images/1.jpg"></image>
							<view class="video-inner">
								<view class="video-title">宠物喂食视频</view>
								<text class="video-text">这是一个宠物喂食的视频，更好的喂食</text>
							</view>	
						</view>
						<view class="home-video-item">
							<image class="video-img" src="/static/images/1.jpg"></image>
							<view class="video-inner">
								<view class="video-title">如何更好的培养宠物感情</view>
								<text class="video-text">这是一个如何更好的培养宠物感情</text>
							</view>	
						</view>	
					</scroll-view>
				</view>	
			</view>	
		</view>	
		
		<!-- 常见问题处理 -->
		<view class="home-issue-block home-top">
			<view class="home-issue">
				<view class="block-title">
					<text class="block-text">常见问题处理</text>
				</view>
				<view class="home-issue-type"> 
					<view class="issue-type">
						<view class="issue-type-item issue-ative"><text>饮食</text></view>
						<view class="issue-type-item"><text>疾病</text></view>
						<view class="issue-type-item"><text>生活用品</text></view>
						<view class="issue-type-item"><text>培养</text></view>
					</view>
					<view class="block-link">更多<text class="iconfont icon-jiantouyou"></text></view>
				</view>
				<view class="home-issue-wrap">
					<view class="home-issue-item">
						<view class="home-issue-inner">
							<view class="home-issue-title">宠物生病该如何认定,该如何紧急救治.</view>
							<view class="home-issue-time">2022-07-13</view>
						</view>	
						<image class="home-issue-img" src="/static/images/1.jpg" mode=""></image>
					</view>	
				</view>	
			</view>	
		</view>
		
		<!-- 附近宠物医院 -->
		<view class="nearby-hospital home-top">
			<view class="home-nearby">
				<view class="block-title">
					<text class="block-text">附近宠物医院</text>
					<view class="block-link">更多<text class="iconfont icon-jiantouyou"></text></view>
				</view>
				<view class="nearby-type">
					<view class="nearby-ative">综合排序</view>
					<view>医院</view>
					<view>店面</view>
					<view>距离优先</view>
					<view>价格优先</view>
					<view>其它</view>
				</view>
				<view class="nearby-wrap">
					<view class="nearby-item">
						<view class="nearby-item-wrap">
							<image class="nearby-img" src="/static/images/1.jpg"></image>
							<view class="nearby-box">
								<view class="nearby-left">
									<view class="nearby-title">联合动物医院</view>
									<view class="nearby-feature">
										<view class="nearby-feature-title">特色:</view>
										<view class="nearby-feature-text">幽门螺旋杆检测</view>
									</view>
									<view class="nearby-position">
										<text class="near-m">303m</text>
										<text class="near-s"></text>
										<view class="nearby-map iconfont icon-fujindianbanben2"></view>
										<text class="near-j">重庆渝中区秋华大道306号</text>
									</view>
									<view class="nearby-praise">
										<view>好评率：<text>4.5</text></view>
										<view>点赞数：<text>3030</text></view>
										<view>收藏量：<text>1030</text></view>
									</view>
								</view>
							</view>
						</view>
					</view>
					<view class="nearby-item">
						<view class="nearby-item-wrap">
							<image class="nearby-img" src="/static/images/1.jpg"></image>
							<view class="nearby-box">
								<view class="nearby-left">
									<view class="nearby-title">联合动物医院</view>
									<view class="nearby-feature">
										<view class="nearby-feature-title">特色:</view>
										<view class="nearby-feature-text">幽门螺旋杆检测</view>
									</view>
									<view class="nearby-position">
										<text class="near-m">303m</text>
										<text class="near-s"></text>
										<view class="nearby-map iconfont icon-fujindianbanben2"></view>
										<text class="near-j">重庆渝中区秋华大道306号</text>
									</view>
									<view class="nearby-praise">
										<view>好评率：<text>4.5</text></view>
										<view>点赞数：<text>3030</text></view>
										<view>收藏量：<text>1030</text></view>
									</view>
								</view>
							</view>
						</view>
					</view>
					<view class="nearby-item">
						<view class="nearby-item-wrap">
							<image class="nearby-img" src="/static/images/1.jpg"></image>
							<view class="nearby-box">
								<view class="nearby-left">
									<view class="nearby-title">联合动物医院</view>
									<view class="nearby-feature">
										<view class="nearby-feature-title">特色:</view>
										<view class="nearby-feature-text">幽门螺旋杆检测</view>
									</view>
									<view class="nearby-position">
										<text class="near-m">303m</text>
										<text class="near-s"></text>
										<view class="nearby-map iconfont icon-fujindianbanben2"></view>
										<text class="near-j">重庆渝中区秋华大道306号</text>
									</view>
									<view class="nearby-praise">
										<view>好评率：<text>4.5</text></view>
										<view>点赞数：<text>3030</text></view>
										<view>收藏量：<text>1030</text></view>
									</view>
								</view>
							</view>
						</view>
					</view>
				</view>
			</view>
			
			<!-- loadmore -->
			<Loadmore :loadmoreState="loadmoreState"></Loadmore>
		</view>
		
		<bar-inset></bar-inset>
	</view>
</template>

<script>
	import BarInset from "@/components/bar-inset/index.vue"
	import Loadmore from "@/components/loadmore/index.vue" // 加载
	export default {
    name: 'Home',
		components: {
			BarInset,
			Loadmore, 
		},
		data() {
			return {
        /* 轮播 */
        carousels: [
					{
						"image" : "/static/images/img1.jpg",
						"title": "标题",
						"info": "这是一个内容"
					},
					{
						"image" : "/static/images/img2.jpg",
						"title": "标题22",
						"info": "这是一个内容222"
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
        loadmoreState: 'loadmore'
			}
		},
		onLoad() {

		},
		methods: {
			imageclick(row){
				console.log('image ---', row)
			}

		}
	}
</script>

<style lang="scss" scoped>
	.home,
	.home-header{
		width: 100%;
		display: block;
	}
	.home-header{
		position: relative;
		.carousel{
			width: 100%;
			height: 430rpx;
			display: block;
			.carousel-item,
			.carousel-image{
				width: 100%;
				height: 100%;
				display: block;
			}
		}
		.home-search{
			width: 100%;
			position: absolute;
			left: 0;
			right: 0;
			bottom: 20rpx;
			padding: 0rpx 50rpx;
			box-sizing: border-box;
			.home-search-box{
				width: 100%;
				// background-color: #ffffff;
				position: relative;
				border-radius: 20rpx;
				display: flex;
				align-items: center;
				padding: 10rpx 0rpx;
				box-sizing: border-box;
				.home-search-icon{
					width: 180rpx;
					height: 70rpx;
					display: flex;
					align-items: center;
					justify-content: center;
					padding: 0rpx 20rpx;
					box-sizing: border-box;
					background-color: #24a7c5;
					border-radius: 50rpx 0rpx 0rpx 50rpx;
					.iconfont{
						font-size: 42rpx;
						color: #ffffff;
						margin-right: 10rpx;
					}
					.home-icon-text{
						max-width: 100rpx;
						// text-align: center;
						font-size: 30rpx;
						color: #ffffff;
						white-space: nowrap;/*内容超宽后禁止换行显示*/
            overflow: hidden;/*超出部分隐藏*/
            text-overflow:ellipsis;/*文字超出部分以省略号显示*/
					}
				}
				.home-search-center{
					flex: 1;
					height: 70rpx;
					line-height: 70rpx;
					display: flex;
					align-items: center;
					background-color: #ffffff;
					border-radius: 0rpx 50rpx 50rpx 0rpx;
					margin-left: 20rpx;
					.home-search-wrap{
						flex: 1;
						display: flex;
						align-items: center;
						padding-left: 20rpx;
						box-sizing: border-box;
						.iconfont{
							font-size: 40rpx;
							color: #606060;
						}
						.home-search-text{
							font-size: 30rpx;
							color: #606060;
							// border-left: 1px solid #dddddd;
							margin-left: 10rpx;
							padding-left: 10rpx;
							box-sizing: border-box;
						}
					}
					.home-search-button{
						width: 120rpx;
						height: 100%;
						text-align: center;
						font-size: 30rpx;
						color: #ffffff;
						background-color: #24a7c5;
						border-radius: 0rpx 50rpx 50rpx 0rpx;
					}
				}
			}
		}
	}
	.home-top{
		margin-top: 50rpx;
	}
	.home-type-block{
	  width: 100%;
		// padding: 0rpx 30rpx;
		box-sizing: border-box;
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
	.column-scroll-view {
		flex-direction: row;
	}
	.home-block{
	  width: 100%;
		padding: 30rpx 30rpx;
		box-sizing: border-box;
		background-color: #ffffff;
		border-radius: 50rpx;
		.home-type{
			width: 100%;
			display: block;
			margin-top: 20rpx;
			white-space:nowrap;
      flex-direction: row;
			position: relative;
			// overflow: hidden;
			// overflow-x: auto;
			.type-item{
				width: 160rpx;
				display: inline-block;
				vertical-align: middle;
				margin-right: 20rpx;
			}
			.type-img{
				width: 100%;
				height: 160rpx;
				border-radius: 10rpx;
			}
			.type-text{
				width: 100%;
				display: block;
				text-align: center;
				margin-top: 5rpx;
				font-size: 28rpx;
				color: #060606;
			}
		}
	}
	.home-video-block{
		width: 100%;
		display: block;
		.home-video{
			width: 100%;
			padding: 30rpx 30rpx;
			box-sizing: border-box;
			background-color: #ffffff;
			border-radius: 50rpx;
			.home-video-content{
				width: 100%;
				display: block;
				margin-top: 20rpx;
				white-space: nowrap;
			}
			.home-video-item{
				width: 600rpx;
				height: 300rpx;
				display: inline-block;
				vertical-align: middle;
				position: relative;
				margin-right: 20rpx;
				.video-img{
					width: 100%;
					height: 100%;
					display: block;
					border-radius: 20rpx;
				}
				.video-inner{
					width: 100%;
					padding: 10rpx 20rpx;
					box-sizing: border-box;
					position: absolute;
					left: 0;
					right: 0;
					bottom: 0;
					z-index: 1;
					.video-title{
						width: 100%;
						font-size: 30rpx;
						color: #ffffff;
					}
					.video-text{
						display: block;
						font-size: 24rpx;
						color: #ffffff;
						margin-top: 10rpx;
					}
				}
			}
		}
	}
	.home-issue-block{
		width: 100%;
		display: block;
		.home-issue{
			width: 100%;
			padding: 30rpx 30rpx;
			box-sizing: border-box;
			background-color: #ffffff;
			border-radius: 50rpx;
		}
		.home-issue-type{
			width: 100%;
			display: flex;
			align-items: center;
			margin-top: 20rpx;
			.issue-type{
				flex: 1;
				display: flex;
				align-items: center;
				white-space: nowrap;
				overflow: hidden;
				overflow-y: auto;
				.issue-type-item{
					font-size: 30rpx;
					color: #060606;
					margin: 0rpx 10rpx;
					position: relative;
					text{
						position: relative;
						z-index: 1;
					}
				}
				.issue-ative{
					&::after{
						content: '';
						width: 100%;
						height: 15rpx;
						background-image: linear-gradient(to right, #1dbfdf, transparent);
						position: absolute;
						left: 0;
						bottom: 0;
						border-radius: 50rpx 0rpx 0rpx 50rpx;
					}
				}
			}
		}
		.home-issue-wrap{
			width: 100%;
			display: block;
			margin-top: 20rpx;
			.home-issue-item{
				width: 100%;
				display: flex;
				// align-items: center;
				padding: 20rpx 0rpx;
				box-sizing: border-box;
				.home-issue-inner{
					flex: 1;
					margin-right: 20rpx;
					display: flex;
					flex-direction: column;
					justify-content: space-between;
					.home-issue-title{
						width: 100%;
						font-size: 30rpx;
						color: #060606;
					}
					.home-issue-time{
						width: 100%;
						font-size: 24rpx;
						color: #999999;
					}
				}
				.home-issue-img{
					width: 230rpx;
					height: 200rpx;
					display: inline-block;
					border-radius: 10rpx;
				}
			}
		}
	}
	.nearby-hospital{
		width: 100%;
		display: block;
		.home-nearby{
			width: 100%;
			padding: 30rpx 30rpx;
			box-sizing: border-box;
			background-color: #ffffff;
			border-radius: 50rpx;
			.nearby-type{
			  width: 100%;
				view{
					width: 150rpx;
					height: 40rpx;
					line-height: 40rpx;
					text-align: center;
					border: 1px solid #f2f2f2;
					border-radius: 50rpx;
					background-color: #f2f2f2;
					font-size: 24rpx;
					color: #666666;
					display: inline-block;
					vertical-align: middle;
					margin-top: 20rpx;
					margin-right: 15rpx;
				}
				.nearby-ative{
					border: 1px solid #1dbfdf;
					background-color: #1dbfdf;
					color: #ffffff;
				}
			}
			.nearby-wrap{
			  width: 100%;
			  display: block;
				.nearby-item{
					width: 100%;
					display: block;
					padding: 30rpx 0rpx;
					box-sizing: border-box;
					.nearby-item-wrap{
						width: 100%;
						display: flex;
						align-items: center;
					}
					.nearby-img{
						width: 150rpx;
						height: 150rpx;
						border-radius: 10rpx;
					}
					.nearby-box{
						flex: 1;
						margin-left: 20rpx;
						display: flex;
						align-items: center;
						.nearby-left{
							flex: 1;
							.nearby-title{
								width: 100%;
								display: block;
								font-size: 32rpx;
								color: #333333;
							}
							.nearby-feature{
								width: 100%;
								display: flex;
								align-items: center;
								.nearby-feature-title{
									font-size: 28rpx;
									color: #333333;
									font-weight: bold;
									margin-right: 10rpx;
								}
								.nearby-feature-text{
									width: 60%;
									font-size: 28rpx;
									color: #333333;
									overflow: hidden;
									text-overflow: ellipsis;
									white-space: nowrap;
								}
							}
							.nearby-position{
								width: 100%;
								display: flex;
								align-items: center;
								margin-top: 10rpx;
								text{
									font-size: 24rpx;
									color: #999999;
									display: inline-block;
								}
								.near-s{
									width: 1px;
									height: 24rpx;
									background-color: #e2e2e2;
									margin: 3rpx 15rpx 0rpx;
								}
								.near-j{
									width: 70%;
									overflow: hidden;
									text-overflow: ellipsis;
									white-space: nowrap;
								}
								.nearby-map{
									font-size: 38rpx;
									color: #999999;
									display: block;
									margin: auto;
								}
							}
							.nearby-praise{
								width: 100%;
								display: flex;
								align-items: center;
								margin-top: 10rpx;
								view{
									font-size: 22rpx;
									color: #999999;
									margin-right: 20rpx;
								}
							}
						}
						/* .nearby-right{
							text-align: center;
							.nearby-map{
								font-size: 54rpx;
								color: #999999;
								display: block;
								margin: auto;
							}
							.nearby-button{
								width: 120rpx;
								height: 46rpx;
								line-height: 46rpx;
								display: block;
								font-size: 24rpx;
								color: #ffffff;
								background-color: #1dbfdf;
								border-radius: 6rpx;
								margin:6rpx auto 0rpx;
							}
						} */
					}
				}
			}
		}
	}
</style>
