<template>
	<view class="search">
		<view class="search-head">
			<u-search placeholder="请输入小区或者学校名" :clearabled="true" :show-action="false" v-model="keyword"></u-search>
		</view>
		<view class="search-type">
			<u-dropdown ref="uDropdown">
				<u-dropdown-item v-model="region" title="区域">
					<view class="slot-content">
						<view class="region-list">
							<u-tabs :list="list.listType" :show-bar="false" :is-scroll="false" :current="current" @change="change" font-size="20"></u-tabs>
							<u-tabs :list="list.listData" :show-bar="false" :current="currentData" @change="changeData" font-size="20"></u-tabs>
							<u-tabs :list="list.listDataDeatail" :show-bar="false" :current="currentDataDeatail" @change="changeDataDeatail"
							 font-size="20"></u-tabs>
						</view>
						<u-button type="primary" @click="closeDropdown">确定</u-button>
					</view>
				</u-dropdown-item>
				<u-dropdown-item v-model="price" title="价格">
					<view class="price-list" style="background-color: #FFFFFF">
						<text style="color: black;font-size: 40rpx;font-weight: bold;">价格区间</text>
						<u-row gutter="12">
							<u-col span="12">
								<u-input style="width: 300rpx;color: #007AFF;" placeholder="请输入价格区间"></u-input>
							</u-col>
							<u-col span="3" class="price-item" v-for="(item,index) in listButton" :key="index">
								<u-button throttle-time="0" style="height: 50rpx;margin: 10rpx;" @click="btnClick(item,$event,index)" :class="{'active':index == nowIndex}">{{item}}</u-button>
							</u-col>
						</u-row>
					</view>
					<u-button type="primary" @click="closeDropdown">确定</u-button>
				</u-dropdown-item>
				<u-dropdown-item v-model="houseType" title="房型">
					<view class="price-list" style="background-color: #FFFFFF">
						<text style="color: black;font-size: 40rpx;font-weight: bold;">房型选择</text>
						<u-row gutter="12">
							<u-col span="3" class="price-item" v-for="(item,index) in listHouseType" :key="index">
								<u-button throttle-time="0" style="height: 50rpx;margin: 10rpx;" @click="btnClickHouse(item,$event,index)"
								 :class="{'active':index == nowHouseIndex}">{{item}}</u-button>
							</u-col>
						</u-row>
					</view>
					<u-button type="primary" @click="closeDropdown">确定</u-button>
				</u-dropdown-item>
				<u-dropdown-item v-model="more" title="更多">
					<view class="price-list" style="background-color: #FFFFFF">
						<text style="color: black;font-size: 40rpx;font-weight: bold;">建筑面积</text>
						<u-row gutter="12">
							<u-col span="3" class="price-item" v-for="(item,index) in moreList.moreListOne" :key="index">
								<u-button throttle-time="0" style="height: 50rpx;margin: 10rpx;" @click="btnClickMoreOne(item,$event,index)"
								 :class="{'active':index == nowMoreOneIndex}">{{item}}</u-button>
							</u-col>
						</u-row>
					</view>
					<view class="price-list" style="background-color: #FFFFFF">
						<text style="color: black;font-size: 40rpx;font-weight: bold;">装修</text>
						<u-row gutter="12">
							<u-col span="3" class="price-item" v-for="(item,index) in moreList.moreListTwo" :key="index">
								<u-button throttle-time="0" style="height: 50rpx;margin: 10rpx;" @click="btnClickMoreTwo(item,$event,index)"
								 :class="{'active':index == nowMoreTwoIndex}">{{item}}</u-button>
							</u-col>
						</u-row>
					</view>
					<view class="price-list" style="background-color: #FFFFFF">
						<text style="color: black;font-size: 40rpx;font-weight: bold;">用途</text>
						<u-row gutter="12">
							<u-col span="3" class="price-item" v-for="(item,index) in moreList.moreListThree" :key="index">
								<u-button throttle-time="0" style="height: 50rpx;margin: 10rpx;" @click="btnClickMoreThree(item,$event,index)"
								 :class="{'active':index == nowMoreThreeIndex}">{{item}}</u-button>
							</u-col>
						</u-row>
					</view>
					<u-button type="primary" @click="closeDropdown">确定</u-button>
				</u-dropdown-item>
				<u-dropdown-item v-model="sortNum" title="排序" :options="options"></u-dropdown-item>
			</u-dropdown>
		</view>
		<view class="search-result">
			<text>已为你搜索到{{65}}房源</text>
		</view>
		<ItemList></ItemList>
	</view>
</template>

<script>
	import ItemList from "components/ItemList/ItemList.vue"
	export default {
		data() {
			return {
				keyword: "",
				region: "",
				price: "",
				houseType: "",
				more: "",
				sortNum: "",
				listButton: ["500以下", "500-1000", "1000-1500", "1500-2000", "2000"],
				listHouseType: ["一室", "两室", "三室", "四室", "五室", "五室以上"],
				moreList: {
					moreListOne: ["30m²以下", "30m²-50m", "50m²-70m", "70m²-90m²", "90m²-120m²", "120m²-150m²", "150m²-200m²",
						"200m²-300m²", "300m²以上"
					],
					moreListTwo: ["精装修", "普通装修", "毛坯房"],
					moreListThree: ["普通住宅", "商业类", "别墅", "四合院", "车位", "其他"]
				},
				options: [{
						label: '默认排序',
						value: 1,
					},
					{
						label: '最新发布',
						value: 2,
					},
					{
						label: '总价从低到高',
						value: 3,
					},
					{
						label: '总价从高到低',
						value: 4,
					},
					{
						label: '面积从大到小',
						value: 5,
					},
				],
				list: {
					listType: [{
							name: "区域"
						},
						{
							name: "地铁"
						}
					],
					listData: [{
							name: "不限"
						},
						{
							name: "江北"
						},
						{
							name: "渝北"
						},
						{
							name: "南岸"
						},
						{
							name: "南岸"
						},
						{
							name: "南岸"
						},
						{
							name: "南岸"
						},
						{
							name: "南岸"
						},
						{
							name: "南岸"
						},
					],
					listDataDeatail: [{
							name: "不限"
						},
						{
							name: "北滨路"
						},
						{
							name: "北滨路"
						},
					]
				},
				current: 0,
				currentData: 0,
				currentDataDeatail: 0,
				btnColor: "",
				nowIndex: null,
				nowHouseIndex: null,
				nowMoreOneIndex: null,
				nowMoreTwoIndex: null,
				nowMoreThreeIndex: null
			}
		},
		components: {
			ItemList
		},
		methods: {
			change(index) {
				this.current = index;
			},
			changeData(index) {
				this.currentData = index;
			},
			changeDataDeatail(index) {
				this.currentDataDeatail = index;
			},
			closeDropdown() {
				this.$refs.uDropdown.close();
				console.log(this.$refs.uDropdown)
			},
			btnClick(item, e, index) {
				console.log(item)
				console.log(e.target)
				this.nowIndex = index
			},
			btnClickHouse(item, e, index) {
				this.nowHouseIndex = index
			},
			btnClickMoreOne(item, e, index) {
				this.nowMoreOneIndex = index
			},
			btnClickMoreTwo(item, e, index) {
				this.nowMoreTwoIndex = index
			},
			btnClickMoreThree(item, e, index) {
				this.nowMoreThreeIndex = index
			}
		}
	}
</script>

<style lang="less" scoped>
	.active {
		background-color: blue;
	}

	.search {
		padding: 30rpx;

		.search-head {}

		.search-type {
			.price-list {
				.price-item {
					button {
						font-size: 20rpx;
						background-color: #F8F8F8;
					}

					.active {
						color: #3072F6;
						font-size: 30rpx;
						font-weight: bold;
						background-color: #EAF1FE;
					}
				}
			}
		}

		.search-result {
			padding-top: 30rpx;
		}
	}
</style>
