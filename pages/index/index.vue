<template>
	<view class="content">
		<view>
			<template>
				<Home v-if="tabName === 'home'"></Home>
				<Classroom v-else-if="tabName === 'classroom'"></Classroom>
				<Hospital v-else-if="tabName === 'hospital'"></Hospital>
				<Registered v-else-if="tabName === 'registered'"></Registered>
				<Personal v-else-if="tabName === 'personal'"></Personal>
			</template>
		</view>
		
		<!-- 底部导航 -->
		<tab-bar :tabList="tabList" @tabChange="tabChange"></tab-bar>
	</view>
</template>

<script>
	import Home from './tabs/home/index'
	import Classroom from './tabs/classroom/index'
	import Hospital from './tabs/hospital/index'
	import Registered from './tabs/registered/index'
	import Personal from './tabs/personal/index'
	
	import tabBar from "@/components/tabBar/index.vue";
	export default {
		components: {
			Home, // 首页
			Classroom, // 课堂
			Hospital, // 附近医院
			Registered, // 挂号就诊
			Personal, // 个人中心
			"tab-bar": tabBar,
		},
		data() {
			return {
				tabList:[
					{
						"name": "home",
						"icon":"icon-shouyefill",
						"text":"首页",
						"url": "/page/index/index" 
					},
					{
						"name": "classroom",
						"icon":"icon-shipin6",
						"text":"讲堂",
						"url": "/page/classroom/index" 
					},
					{
						"name": "hospital",
						"icon":"icon-yiyuan-2",
						"text":"附近医院",
						"url": "/page/hospital/index" 
					},
					{
						"name": "registered",
						"icon":"icon-chongwutubiao18",
						"text":"挂号就诊",
						"url": "/page/registered/index" 
					},
					{
						"name": "personal",
						"icon":"icon-chongwu",
						"text":"我的",
						"url": "/page/personal/index" 
					},
				],
				tabName: 'home'
			}
		},
		onLoad() {

		},
		methods: {
			// tab点击
			tabChange(index){
				console.log('tab点击', index)
				this.tabName = this.tabList[index].name
			},

		}
	}
</script>

<style lang="scss" scoped>
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
