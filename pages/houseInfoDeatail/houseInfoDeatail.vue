<template>
	<view class="house-info">
		<view class="">
			<u-swiper :list="list" height="400" mode="number" indicator-pos="bottomRight"></u-swiper>
		</view>
		<view class="house-main">
			<view class="house-title">
				<p>2299元/月（季付）</p>
				<p>整租 · 汇祥林里3000四期 3室2厅</p>
			</view>
			<view class="house-deatail">
				<u-row gutter="12">
					<u-col span="3" class="house-tro">
						<p>东 东南</p>
						<p>朝向</p>
					</u-col>
					<u-col span="3" class="house-tro">
						<p>120m²</p>
						<p>面积</p>
					</u-col>
					<u-col span="3" class="house-tro">
						<p>17/32层</p>
						<p>楼层</p>
					</u-col>
					<u-col span="3" class="house-tro">
						<p>随时入住</p>
						<p>入住时间</p>
					</u-col>
				</u-row>
			</view>
			<view class="house-tag">
				<u-button size="mini" type="info" :hair-line="false">近地铁</u-button>
				<u-button size="mini" type="info" :hair-line="false">精装修</u-button>
				<u-button size="mini" type="info" :hair-line="false">双卫生间</u-button>
				<u-button size="mini" type="info" :hair-line="false">有车位</u-button>
				<u-button size="mini" type="info" :hair-line="false">有电梯</u-button>
				<u-button size="mini" type="info" :hair-line="false">可月租</u-button>
				<u-button size="mini" type="info" :hair-line="false">名水电</u-button>
				<u-button size="mini" type="info" :hair-line="false">随时看房</u-button>
				<u-button size="mini" type="info" :hair-line="false">租住保障</u-button>
			</view>
			<view class="hosue-init">
				<u-row gutter="12">
					<u-col span="7">
						<p><text style="font-weight: bold;">租期：</text>2-8个月</p>
					</u-col>
					<u-col span="3" offset="2">
						<text style="color: #5373B2;">咨询租期</text>
						<text style="color: #CDCDCD;">&gt;</text>
					</u-col>
				</u-row>
				<u-row gutter="12">
					<u-col span="7">
						<p><text style="font-weight: bold;">看房：</text>随时可看</p>
					</u-col>
					<u-col span="3" offset="2">
						<text style="color: #5373B2;">咨询看房</text>
						<text style="color: #CDCDCD;">&gt;</text>
					</u-col>
				</u-row>
				<u-row gutter="12">
					<u-col span="7">
						<p><text style="font-weight: bold;">风险提示：</text>用户风险提示</p>
					</u-col>
					<u-col span="3" offset="2">
						<text style="color: #5373B2;">查看提示</text>
						<text style="color: #CDCDCD;">&gt;</text>
					</u-col>
				</u-row>
				<u-row gutter="12">
					<u-col span="7">
						<p><text style="font-weight: bold;">家缘投诉电话：</text>用户风险提示</p>
					</u-col>
					<u-col span="3" offset="2">
						
					</u-col>
				</u-row>
			</view>
			<u-gap height="30" bg-color="#F8F8F9"></u-gap>
			<view class="house-intro">
				<text style="font-size: 40rpx;">房源简介</text>
				<u-row gutter="12" class="house-icons">
					<u-col span="2" class="house-icon">
						<u-icon label="电视" top="0" label-pos="bottom" size="50" name="/static/iconHouseIntro/电视.png"></u-icon>
					</u-col>
					<u-col span="2" class="house-icon">
						<u-icon label="冰箱" size="50" label-pos="bottom" name="/static/iconHouseIntro/冰箱.png"></u-icon>
					</u-col>
					<u-col span="2" class="house-icon">
						<u-icon label="洗衣机" size="50" label-pos="bottom" name="/static/iconHouseIntro/洗衣机.png"></u-icon>
					</u-col>
					<u-col span="2" class="house-icon">
						<u-icon label="空调" size="50" label-pos="bottom" name="/static/iconHouseIntro/空调.png"></u-icon>
					</u-col>
					<u-col span="2" class="house-icon">
						<u-icon label="热水器" size="50" label-pos="bottom" name="/static/iconHouseIntro/热水器_1.png"></u-icon>
					</u-col>
					<u-col span="2" class="house-icon">
						<u-icon label="床" size="50" label-pos="bottom" name="/static/iconHouseIntro/床.png"></u-icon>
					</u-col>
					<u-col span="2" class="house-icon">
						<u-icon label="暖气" size="50" label-pos="bottom" name="/static/iconHouseIntro/暖气.png"></u-icon>
					</u-col>
					<u-col span="2" class="house-icon">
						<u-icon label="宽带" size="50" label-pos="bottom" name="/static/iconHouseIntro/宽带.png"></u-icon>
					</u-col>
					<u-col span="2" class="house-icon">
						<u-icon label="衣柜" size="50" label-pos="bottom" name="/static/iconHouseIntro/衣柜.png"></u-icon>
					</u-col>
					<u-col span="2" class="house-icon">
						<u-icon label="天然气" size="50" label-pos="bottom" name="/static/iconHouseIntro/天然气.png"></u-icon>
					</u-col>
				</u-row>
			</view>
			<text style="font-size: 40rpx;">费用详情</text>
			<view class="house-deatail">
				<text style="font-size: 30rpx;color: red;">年租价</text>
				<u-row gutter="12">
					<u-col span="3" class="house-tro">
						<p>付款方式</p>
						<p>月付</p>
					</u-col>
					<u-col span="2" class="house-tro">
						<p>租金</p>
						<p>2299</p>
					</u-col>
					<u-col span="2" class="house-tro">
						<p>押金</p>
						<p>3000</p>
					</u-col>
					<u-col span="3" class="house-tro">
						<p>服务费</p>
						<p>0</p>
					</u-col>
					<u-col span="2" class="house-tro">
						<p>中介费</p>
						<p>0</p>
					</u-col>
				</u-row>
				<text style="font-size: 30rpx;color: red;">月租价</text>
				<u-row gutter="12">
					<u-col span="3" class="house-tro">
						<p>付款方式</p>
						<p>月付</p>
					</u-col>
					<u-col span="2" class="house-tro">
						<p>租金</p>
						<p>2299</p>
					</u-col>
					<u-col span="2" class="house-tro">
						<p>押金</p>
						<p>3000</p>
					</u-col>
					<u-col span="3" class="house-tro">
						<p>服务费</p>
						<p>0</p>
					</u-col>
					<u-col span="2" class="house-tro">
						<p>中介费</p>
						<p>0</p>
					</u-col>
				</u-row>
			</view>
			<view class="" style="padding-bottom: 100rpx;margin-top: 20rpx;">
				<text>请评分</text>
				<u-rate :count="count" v-model="value"></u-rate>
			</view>
		</view>
		<view class="house-footer">
			<view class="main">
				<u-row gutter="12" justify="flex-end">
					<u-col span="4" style="text-align: center;margin-top: 10rpx;">
						<u-icon name="heart" size="50"></u-icon>
						<u-icon name="share" size="50" style="margin-left: 50rpx;"></u-icon>
					</u-col>
					<u-col span="4">
						<u-button type="success" :ripple="true">在线咨询</u-button>
					</u-col>
					<u-col span="4">
						<u-button type="primary" :ripple="true">电话咨询</u-button>
					</u-col>
				</u-row>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				count:5,
				value:2,
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
	.house-info {
		.house-footer{
			position: fixed;
			bottom: 0;
			height: 100rpx;
			width: 100%;
			background-color: #FFFFFF;
			.main{
				line-height: 100rpx;
			}
		}
		.house-main {
			view {
				padding: 5rpx;
			}

			padding: 30rpx;

			.house-title {
				p {
					font-size: 40rpx;
					font-weight: bold;

					&:nth-child(2) {
						font-size: 30rpx;
					}

					&:nth-child(1) {
						color: #FF0000;
					}
				}
			}

			.house-deatail {
				border-top: 2rpx solid #E4E6F0;
				border-bottom: 2rpx solid #E4E6F0;
				padding: 30rpx;

				.house-tro {
					p {
						&:nth-child(1) {
							font-size: 30rpx;
						}

						&:nth-child(2) {
							margin-top: 10rpx;
							font-size: 20rpx;
							color: #A1A7B1;
						}
					}
				}
			}

			.house-tag {
				padding: 30rpx 0;

				.u-btn {
					margin: 10rpx;
				}
			}
			.house-intro{
				padding: 30rpx 0;
				margin: 0 10rpx;
				.house-icons{
					.house-icon{
						margin: 20rpx;
					}
				}
				
			}
		}
	}
</style>
