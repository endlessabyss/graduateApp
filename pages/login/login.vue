<template>
	<view class="login">
		<text>登录</text>
		<view class="login-form">
			<u-form :model="form" ref="uForm">
				<u-form-item prop="name">
					<u-input v-model="form.name" placeholder="请输入手机号" />
				</u-form-item>
				<u-form-item prop="intro">
					<u-input v-model="form.intro" placeholder="请输入密码" />
				</u-form-item>
			</u-form>
			<u-button @click="submit" type="primary">登录</u-button>
		</view>
		<view class="">
			<p>其他登录方式</p>
			<u-icon name="weixin-fill" color="#00aa00" size="60"></u-icon>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				form: {
					name: '',
					intro: '',
				},
				rules: {
					name: [{
						required: true,
						message: '请输入姓名',
						// 可以单个或者同时写两个触发验证方式 
						trigger: ['change', 'blur'],
					}],
					intro: [{
						min: 5,
						message: '简介不能少于5个字',
						trigger: 'change'
					}]
				}
			};
		},
		methods: {
			submit() {
				this.$refs.uForm.validate(valid => {
					if (valid) {
						console.log('验证通过');
					} else {
						console.log('验证失败');
					}
				});
			}
		},
		// 必须要在onReady生命周期，因为onLoad生命周期组件可能尚未创建完毕
		onReady() {
			this.$refs.uForm.setRules(this.rules);
		}
	};
</script>

<style lang="less" scoped>
.login{
	text-align: center;
	text{
		font-size: 50rpx;
		font-weight: bold;
	}
	.login-form{
		padding: 30rpx;
	}
}
</style>
