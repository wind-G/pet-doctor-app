<template>
	<view class="hospital">
		<!-- <Inset></Inset> -->
		<!-- 搜索 -->
		<view class="hospital-search" style="margin-top: 56rpx;">
			<view class="hospital-search-box">
				<view class="hospital-search-icon">
					<view class="iconfont icon-fujinjihuo"></view>
					<view class="hospital-icon-text">重庆</view>
				</view>
				<view class="hospital-search-center">
					<view class="hospital-search-wrap">
						<view class="iconfont icon-sousuo2"></view>
						<view class="hospital-search-text">搜索附近宠物医院</view>	
					</view>	
					<view class="hospital-search-button">
						搜索
					</view>
				</view>
			</view>
		</view>
		
		<!-- 本地医院 -->
		<view class="local-hospital">
			<view class="local-hospital-type">
				<view class="local-type-header">
					<view class="local-type-item local-ative">预约挂号</view>
					<view class="local-type-item">体检/检查</view>
					<view class="local-type-item">疫苗接种</view>
				</view>
				<view class="local-type-all">
					<view class="local-type-warp">
						<view class="local-type-in type-ative">综合排序</view>
						<view class="local-type-in">距离优先</view>
						<view class="local-type-in">价格优先</view>
						<view class="local-type-in">好评率</view>
						<view class="local-type-in">点赞率</view>
						<view class="local-type-in">收藏率</view>
						<view class="local-type-in">观看率</view>
						<view class="local-type-in">其它</view>
					</view>
				</view>
			</view>
			<view class="local-hospital-content">
				<view class="local-cont-item">
					<view class="local-cont-top">
						<image class="local-img" src="/static/images/1.jpg"></image>
						<view class="local-box">
							<view class="local-hd">
								<view class="local-title">联合动物医院</view>
								<view class="local-feature">
									<view class="local-feature-title">特色:</view>
									<view class="local-feature-text">幽门螺旋杆检测</view>
								</view>
								<view class="local-position">
									<text class="local-m">303m</text>
									<text class="local-s"></text>
									<view class="local-map iconfont icon-fujindianbanben2"></view>
									<text class="local-j">重庆渝中区秋华大道306号</text>
								</view>
								<view class="local-praise">
									<view>好评率：<text>4.5</text></view>
									<view>点赞数：<text>3030</text></view>
									<view>收藏量：<text>1130</text></view>
								</view>
							</view>
						</view>
					</view>
					<view class="local-footer">
						<view class="local-button">预约挂号</view>
					</view>
				</view>
				<view class="local-cont-item">
					<view class="local-cont-top">
						<image class="local-img" src="/static/images/1.jpg"></image>
						<view class="local-box">
							<view class="local-hd">
								<view class="local-title">联合动物医院</view>
								<view class="local-feature">
									<view class="local-feature-title">特色:</view>
									<view class="local-feature-text">幽门螺旋杆检测</view>
								</view>
								<view class="local-position">
									<text class="local-m">303m</text>
									<text class="local-s"></text>
									<view class="local-map iconfont icon-fujindianbanben2"></view>
									<text class="local-j">重庆渝中区秋华大道306号</text>
								</view>
								<view class="local-praise">
									<view>好评率：<text>4.5</text></view>
									<view>点赞数：<text>3030</text></view>
									<view>收藏量：<text>1130</text></view>
								</view>
							</view>
						</view>
					</view>
					<view class="local-footer">
						<view class="local-button">预约挂号</view>
					</view>
				</view>
				<view class="local-cont-item">
					<view class="local-cont-top">
						<image class="local-img" src="/static/images/1.jpg"></image>
						<view class="local-box">
							<view class="local-hd">
								<view class="local-title">联合动物医院</view>
								<view class="local-feature">
									<view class="local-feature-title">特色:</view>
									<view class="local-feature-text">幽门螺旋杆检测</view>
								</view>
								<view class="local-position">
									<text class="local-m">303m</text>
									<text class="local-s"></text>
									<view class="local-map iconfont icon-fujindianbanben2"></view>
									<text class="local-j">重庆渝中区秋华大道306号</text>
								</view>
								<view class="local-praise">
									<view>好评率：<text>4.5</text></view>
									<view>点赞数：<text>3030</text></view>
									<view>收藏量：<text>1130</text></view>
								</view>
							</view>
						</view>
					</view>
					<view class="local-footer">
						<view class="local-button">预约挂号</view>
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
	import Inset from "@/components/inset/index.vue" // 头部高度
	import BarInset from "@/components/bar-inset/index.vue"
	import Loadmore from "@/components/loadmore/index.vue" // 加载
	export default {
    name: 'Hospital',
		components: {
			Inset,
			BarInset,
			Loadmore,
		},
		data() {
			return {
        loadmoreState: 'loadmore'
			}
		},
    computed: {
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style lang="scss" scoped>
	.hospital{
		width: 100%;
		display: block;
	}
	.hospital-search{
		width: 100%;
		padding: 20rpx 30rpx;
		box-sizing: border-box;
		background-color: #ffffff;
		.hospital-search-box{
			width: 100%;
			height: 70rpx;
			display: flex;
			// border: 1px solid #24a7c5;
			// border-radius: 10rpx;
			position: relative;
			.hospital-search-icon{
				width: 160rpx;
				display: flex;
				align-items: center;
				justify-content: center;
				padding: 0rpx 10rpx;
				box-sizing: border-box;
				background-color: #24a7c5;
				border-radius: 20rpx 0rpx 0rpx 20rpx;
				.iconfont{
					font-size: 42rpx;
					color: #ffffff;
					margin-right: 10rpx;
				}
				.hospital-icon-text{
					max-width: 100rpx;
					// text-align: center;
					font-size: 30rpx;
					color: #ffffff;
					white-space: nowrap;/*内容超宽后禁止换行显示*/
					overflow: hidden;/*超出部分隐藏*/
					text-overflow:ellipsis;/*文字超出部分以省略号显示*/
				}
			}
			.hospital-search-center{
				flex: 1;
				height: 70rpx;
				line-height: 70rpx;
				display: flex;
				align-items: center;
				background-color: #ffffff;
				border-radius: 0rpx 20rpx 20rpx 0rpx;
				border-top: 1px solid #24a7c5;
				border-bottom: 1px solid #24a7c5;
				box-sizing: border-box;
				overflow: hidden;
				.hospital-search-wrap{
					flex: 1;
					display: flex;
					align-items: center;
					padding-left: 20rpx;
					box-sizing: border-box;
					.iconfont{
						font-size: 40rpx;
						color: #606060;
					}
					.hospital-search-text{
						font-size: 30rpx;
						color: #606060;
						// border-left: 1px solid #dddddd;
						margin-left: 10rpx;
						padding-left: 10rpx;
						box-sizing: border-box;
					}
				}
				.hospital-search-button{
					width: 140rpx;
					height: 100%;
					text-align: center;
					font-size: 30rpx;
					color: #ffffff;
					background-color: #24a7c5;
				}
			}
		}
	}
	.local-hospital{
		width: 100%;
		display: block;
		.local-hospital-type{
			width: 100%;
			display: block;
			background-color: #ffffff;
			padding: 0rpx 30rpx;
			box-sizing: border-box;
			.local-type-header{
				width: 100%;
				display: flex;
				justify-content: space-between;
				border-bottom: 1px solid #f2f2f2;
				.local-type-item{
					display: inline-block;
					padding: 0rpx 30rpx 20rpx;
					box-sizing: border-box;
					font-size: 28rpx;
					color: #333333;
					position: relative;
				}
				.local-ative{
					font-weight: bold;
					color: #24a7c5;
					&::after{
						content: '';
						width: 40rpx;
						height: 6rpx;
						display: block;
						border-radius: 50rpx;
						background-color: #24a7c5;
						position: absolute;
						left: 0;
						right: 0;
						bottom: 0;
						z-index: 1;
						margin: auto;
					}
				}
			}
			.local-type-all{
				width: 100%;
				display: block;
				.local-type-warp{
					width: 100%;
					display: flex;
					flex-wrap: wrap;
					justify-content: flex-start;
					padding: 20rpx 0rpx;
					.local-type-in{
						width: 23%;
						height: 50rpx;
						line-height: 46rpx;
						margin: 10rpx 1%;
						text-align: center;
						border: 1px solid #f2f2f2;
						background-color: #f2f2f2;
						border-radius: 50rpx;
						box-sizing: border-box;
						font-size: 24rpx;
						color: #666666;
					}
					.type-ative{
						border: 1px solid #24a7c5;
						color: #24a7c5;
						background-color: #ffffff;
					}
				}
			}
		}
		.local-hospital-content{
			width: 100%;
			display: block;
			padding: 10rpx 30rpx 0rpx;
			box-sizing: border-box;
			.local-cont-item{
				width: 100%;
				display: block;
				padding: 30rpx 30rpx;
				box-sizing: border-box;
				background-color: #ffffff;
				border-radius: 20rpx;
				margin-top: 20rpx;
				.local-cont-top{
					width: 100%;
					display: flex;
					align-items: center;
				}
				.local-img{
					width: 150rpx;
					height: 150rpx;
					border-radius: 10rpx;
				}
				.local-box{
					flex: 1;
					margin-left: 20rpx;
					display: flex;
					align-items: center;
					.local-hd{
						flex: 1;
						.local-title{
							width: 100%;
							display: block;
							font-size: 32rpx;
							color: #333333;
						}
						.local-feature{
							width: 100%;
							display: flex;
							align-items: center;
							.local-feature-title{
								font-size: 28rpx;
								color: #333333;
								font-weight: bold;
								margin-right: 10rpx;
							}
							.local-feature-text{
								width: 60%;
								font-size: 28rpx;
								color: #333333;
								overflow: hidden;
								text-overflow: ellipsis;
								white-space: nowrap;
							}
						}
						.local-position{
							width: 100%;
							display: flex;
							align-items: center;
							text{
								font-size: 24rpx;
								color: #999999;
								display: inline-block;
							}
							.local-s{
								width: 1px;
								height: 24rpx;
								background-color: #e2e2e2;
								margin: 3rpx 15rpx 0rpx;
							}
							.local-j{
								width: 70%;
								overflow: hidden;
								text-overflow: ellipsis;
								white-space: nowrap;
							}
							.local-map{
								font-size: 38rpx;
								color: #999999;
								display: block;
								margin: auto;
							}
						}
						.local-praise{
							width: 100%;
							display: flex;
							align-items: center;
							margin-top: 10rpx;
							view{
								font-size: 24rpx;
								color: #999999;
								margin-right: 20rpx;
							}
						}
					}
				}
				.local-footer{
					width: 100%;
					display: block;
					border-top: 1px solid #f2f2f2;
					text-align: right;
					margin-top: 20rpx;
					padding-top: 20rpx;
					box-sizing: border-box;
					.local-button{
						width: 160rpx;
						height: 56rpx;
						line-height: 56rpx;
						text-align: center;
						display: inline-block;
						font-size: 28rpx;
						color: #ffffff;
						background-color: #1dbfdf;
						border-radius: 6rpx;
						margin: 0rpx 20rpx;
					}
				}
			}
		}
	}
</style>
