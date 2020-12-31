<template>
	<view class="item-list">
		<u-row gutter="12" style="padding-top: 10rpx;">
			<u-col span="4">
				<text class="" style="font-size: 40rpx;font-weight: bold;">
					房源信息
				</text>
			</u-col>
		</u-row>
		<u-row gutter="12" style="padding-top: 20rpx;" class="item" v-for="index in 20" :key="index">
			<u-col span="5">
				<u-image width="100%" height="200rpx" src="https://ss1.bdstatic.com/70cFuXSh_Q1YnxGkpoWK1HF6hhy/it/u=807281771,3921567376&fm=26&gp=0.jpg"></u-image>
			</u-col>
			<u-col span="7" class="item-right">
				<u-col span="12" class="item-child">
					<text>渝北中央公园。门口轻9号 10号 香港置地，安静</text>
				</u-col>
				<u-col span="12" class="item-child">
					<text>3室2厅/106.63m²/东南/公园大道上东汇菁澜</text>
				</u-col>
				<u-col span="12" class="item-child">
					<text>随时看房</text>
					<text>看装修</text>
				</u-col>
				<u-col span="12" class="item-child">
					<text>1500/月</text>
					<text>88m²</text>
				</u-col>
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
	.item-list {
		.item {
			.item-right {
				padding: 0 20rpx;
				.item-child{
					margin-top: 5rpx;
					&:nth-child(1){
						font-size: 30rpx;
						font-weight: bold;
					}
					&:nth-child(2){
						font-size: 20rpx;
						white-space: nowrap;
						text-overflow: ellipsis;
						overflow: hidden;
					}
					&:nth-child(3){
						text{
							margin: 10rpx;
							font-size: 10rpx;
							border-radius: 5rpx;
							display: inline-block;
							color: #869BAF;
							background-color: #E5EAED;
						}
					}
					&:nth-child(4){
						text{
							&:nth-child(1){
								color: red;
								font-weight: bold;
								font-size: 30rpx;
							}
							&:nth-child(2){
								color: #ADADAD;
								margin-left: 6rpx;
								font-size: 20rpx;
							}
						}
					}
				}
			}
		}
	}
</style>
