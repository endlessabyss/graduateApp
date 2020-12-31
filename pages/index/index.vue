<template>
	<view class="app">
		<view class="content">
			<view class="text-search">
				<view class="search">
					<view class="" @tap="handleSearch">
						<u-search placeholder="你想住在哪" v-model="keyword" :show-action="false"></u-search>
					</view>
					<view class="">
						<u-icon name="map-fill" color="blue" size="40rpx" class="icon-map" label="重庆" @click="mapSlect"></u-icon>
					</view>
				</view>
			</view>
		</view>
		<view class="wrap">
			<u-row gutter="12">
				<u-col span="3" class="item-action">
					<view>
						<image src="/static/typeMacket/rent.png" mode="aspectFit">
							<view class="text-action">
								<text>租房</text>
							</view>
					</view>
				</u-col>
				<u-col span="3" class="item-action">
					<view>
						<image src="/static/typeMacket/short.png" mode="aspectFit">
							<view class="text-action">
								<text>短租</text>
							</view>
					</view>
				</u-col>
				<u-col span="3" class="item-action">
					<view>
						<image src="/static/typeMacket/long.png" mode="aspectFit">
							<view class="text-action">
								<text>长租</text>
							</view>
					</view>
				</u-col>
				<u-col span="3" class="item-action">
					<view>
						<image src="/static/typeMacket/coales.png" mode="aspectFit">
							<view class="text-action">
								<text>合租</text>
							</view>
					</view>
				</u-col>
			</u-row>
		</view>
		<view class="look-house">
			<text class="title">帮我找房</text>
			<view class="look-detail">
				<u-row gutter="12">
					<u-col span="6">

					</u-col>
					<u-col span="6">
						<u-col span="6">
							<text>

							</text>
						</u-col>
						<u-col span="6">
							<text>

							</text>
						</u-col>
					</u-col>
				</u-row>
			</view>
		</view>
		<u-select v-model="show" mode="mutil-column-auto" :list="list" @confirm="mapSlect"></u-select>
		<HouseList />
	</view>
</template>

<script>
	import HouseList from "components/houseList/houseList";
	export default {
		data() {
			return {
				keyword: '',
				show: false,
				list: [{
						value: 1,
						label: '中国',
						children: [{
								value: 2,
								label: '广东',
								children: [{
										value: 3,
										label: '深圳'
									},
									{
										value: 4,
										label: '广州'
									}
								]
							},
							{
								value: 5,
								label: '广西',
								children: [{
										value: 6,
										label: '南宁'
									},
									{
										value: 7,
										label: '桂林'
									}
								]
							}
						]
					},
					{
						value: 8,
						label: '美国',
						children: [{
							value: 9,
							label: '纽约',
							children: [{
								value: 10,
								label: '皇后街区'
							}]
						}]
					}
				]
			}
		},
		onLoad() {

		},
		components: {
			HouseList
		},
		methods: {
			handleSearch() {
				console.log("d")
				uni.navigateTo({
					url: '/pages/searchInfo/searchInfo'
				});
			},
			mapSlect(e) {
				console.log(1)
				this.show = true
			}
		}
	}
</script>

<style lang="less" scoped>
	.app {
		.content {
			width: 100%;
			height: 400rpx;
			background-repeat: no-repeat;
			overflow: hidden;
			background-size: 100%;
			background-image: url(@~static/img/iu.jpg);

			.text-search {
				margin: 30rpx;

				.search {
					position: relative;

					.icon-map {
						position: absolute;
						right: 60rpx;
						top: 15rpx;
					}
				}
			}
		}

		.wrap {
			.item-action {
				text-align: center;

				image {
					width: 80rpx;
					height: 80rpx;
					padding: 50rpx;
					padding-bottom: 0;
				}

				.text-action {
					font-size: 20rpx;
					text-align: center;
				}
			}
		}

		.look-house {
			padding: 50rpx;

			.title {
				font-size: 40rpx;
				font-weight: bold;
			}

			.look-detail {
				padding: 50rpx;
				margin-top: 20rpx;
				width: 100%;
				height: 200rpx;
				border-radius: 10rpx;
				border: 5rpx solid #f0f0f0;
				background-image: url('https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fa0.att.hudong.com%2F52%2F62%2F31300542679117141195629117826.jpg&refer=http%3A%2F%2Fa0.att.hudong.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=jpeg?sec=1611476672&t=b3edeeddbeb70de4f0496d28758f8065');
				background-repeat: no-repeat;
				background-size: 100%;
				color: red;
			}
		}
	}
</style>
