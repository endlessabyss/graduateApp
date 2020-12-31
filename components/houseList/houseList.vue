<template>
	<view>
		<view class="look-info">
			<u-row gutter="12">
				<u-col span="4">
					<text class="" style="font-size: 40rpx;font-weight: bold;">
						附近房源
					</text>
				</u-col>
			</u-row>
			<text>走过路过，千万不要错过........！！！！！！！！</text>
			<u-row gutter="12">
				<u-col span="12">
					<u-swiper :list="list" :title="true" :circular="false"></u-swiper>
				</u-col>
			</u-row>
			<ItmeList></ItmeList>
		</view>
	</view>
</template>

<script>
	import ItmeList from "components/ItemList/ItemList"
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
		components:{
			ItmeList
		},
		methods: {
			
		}
	}
</script>

<style lang="less" scoped>
	.look-info{
		padding: 50rpx;
		padding-top: 0;
	}
</style>
