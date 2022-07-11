<template>
	<view class="content">
		bbb
		<!-- 底部导航 -->
		<tab-bar :fixed-bottom="false"></tab-bar>
	</view>
</template>

<script>
	import tabBar from "@/components/tabBar/index.vue";
	export default {
		components: {
			"tab-bar": tabBar,
		},
		data() {
			return {
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>
	.content {
		/* display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center; */
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
</style>
