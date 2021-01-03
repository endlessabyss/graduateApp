<template>
	<view class="my-info">
		<view class="login">
			<u-row gutter="12">
				<u-col span="2">
					<u-avatar :src="src"></u-avatar>
				</u-col>
				<u-col span="8">
					<view style="font-size: 40rpx;color: #FFFFFF;" @click="loginRegister">
						点击登录/注册
					</view>
				</u-col>
			</u-row>
		</view>
		<u-row gutter="12" class="type">
			<u-col span="4" class="item-type">
				<u-icon label="订阅" label-pos="bottom" size="80" name="/static/my/订阅.png"></u-icon>
			</u-col>
			<u-col span="4" class="item-type">
				<u-icon label="关注" label-pos="bottom" size="80" name="/static/my/关注.png"></u-icon>
			</u-col>
			<u-col span="4" class="item-type">
				<u-icon label="最近浏览" label-pos="bottom" size="80" name="/static/my/最近浏览.png"></u-icon>
			</u-col>
		</u-row>
		<u-gap height="20" bg-color="#ebebeb"></u-gap>
		<u-row gutter="12" class="action-type" v-for="(item,index) in 10" :key="index">
			<u-col span="1">
				<u-icon name="file-text-fill" size="28"></u-icon>
			</u-col>
			<u-col span="11" class="action-item">
				<u-section font-size="30" :bold="false" title="我的钱包" :show-line="false" sub-title=""></u-section>
			</u-col>
		</u-row>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				src: 'http://pic2.sc.chinaz.com/Files/pic/pic9/202002/hpic2119_s.jpg',
			}
		},
		methods: {
			loginRegister(){
				uni.navigateTo({
					url: "/pages/login/login"
				})
			}
		}
	}
</script>

<style lang="less" scoped>
	.my-info {
		.login {
			padding: 40rpx;
			background-color: #3475F7;
		}

		.type {
			padding: 30rpx;

			.item-type {
				padding: 50rpx !important;
			}
		}

		.action-type {
			padding: 20rpx;
			.action-item {
				border-bottom: 2rpx solid #e6e6e6;
				padding: 30rpx 0 !important;
			}
		}
	}
</style>
