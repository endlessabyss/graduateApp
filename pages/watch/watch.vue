<template>
	<view>
		<view class="item" v-for="(item,index) in 20" :key="index">
			<view class="wrap">
				<u-swiper :list="list" height="300"></u-swiper>
				<view class="wrap-item">
					<u-row gutter="12">
						<u-col span="8">
							4居室 南卧 B区
						</u-col>
						<u-col span="4" style="color: red;">
							800元/月
						</u-col>
						<u-col span="12" style="padding: 20rpx 0;">
							户型南北通透，全全明格局，名厨名为，房子楼梯高楼层！采光好！小区环境好！价格合适。
						</u-col>
					</u-row>
					<u-row gutter="12">
						<u-col span="2">
							<u-avatar src="https://ss2.bdstatic.com/70cFvnSh_Q1YnxGkpoWK1HF6hhy/it/u=1782192750,2489466674&fm=26&gp=0.jpg" mode="circle"></u-avatar>
						</u-col>
						<u-col span="7">
							<view style="font-size: 30rpx;font-weight: bold;">
								曾繁荣
							</view>
							<view style="color: #CCCCCC;font-size: 20rpx;">
								房源信息找我咨询
							</view>
						</u-col>
						<u-col span="3">
							<u-icon size="40" style="padding: 20rpx;" name="chat-fill"></u-icon>
							<u-icon size="40" style="padding: 10rpx;" name="phone-fill"></u-icon>
						</u-col>
					</u-row>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				list: [{
						image: 'https://cdn.uviewui.com/uview/swiper/1.jpg',
						title: '昨夜星辰昨夜风，画楼西畔桂堂东'
					},
					{
						image: 'https://cdn.uviewui.com/uview/swiper/2.jpg',
						title: '身无彩凤双飞翼，心有灵犀一点通'
					},
					{
						image: 'https://cdn.uviewui.com/uview/swiper/3.jpg',
						title: '谁念西风独自凉，萧萧黄叶闭疏窗，沉思往事立残阳'
					}
				],
			}
		},
		methods: {

		}
	}
</script>

<style lang="less" scoped>
	.item {
		padding: 30rpx;

		.wrap {
			.wrap-item {
				padding: 20rpx;
				background-color: #FFFFFF;
				box-shadow: 0px 0px 5px skyblue;
			}
		}
	}
</style>
