<template>
	<view class="info">
		<u-row gutter="12" class="info-item" v-for="(item,index) in 20" :key="index">
			<u-col span="2" style="position: relative;">
				<u-badge type="error" count="7" size="mini"></u-badge>
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
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="less" scoped>
.info{
	.info-item{
		background-color: #dcdddf;
		margin: 10rpx 0;
	}
}
</style>
