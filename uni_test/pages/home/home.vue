<template>
	<view>
		<uni-nav-bar color="#333333" background-color="#FFFFFF" fixed="false" @click-left="showCity"
		 @click-right="scan">
			<block slot="left">
				<view class="navbarFreeIcon">
					<uni-icon type="bars" color="#eee" size="22"></uni-icon>
					<br>
					<text>分类</text>
				</view>
			</block>
			<view class="input-view">
				<uni-icon type="search" size="22" color="#666666"></uni-icon>
				<input confirm-type="search" @confirm="confirm" class="input" type="text" placeholder="输入搜索关键词" />
			</view>
			<block slot="right">
				<view class="navbarFreeIcon">
					<uni-icon type="chat" color="#eee" size="22"></uni-icon>
					<text>信息</text>
				</view>
			</block>
		</uni-nav-bar>
		<swiper class="swiper" :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval" :duration="duration">
			<swiper-item>
				<view class="swiper-item uni-bg-red">A</view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item uni-bg-green">B</view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item uni-bg-blue">C</view>
			</swiper-item>
			 
		</swiper>
		<view class="free_grid">
			<view class="free_grid_1">
				<navigator  url="/pages/index/index" hover-class="navigator-hover">
					<image class="img" mode='widthFix'  src="../../static/1.png"></image>
					<view class="name">bbb</view>
				</navigator>
			</view>
			<view class="free_grid_1">
				<navigator open-type="switchTab" url="/pages/cart/cart" hover-class="navigator-hover">
				<image class="img" mode='widthFix'  src="../../static/1.png"></image><view class="name">bbb</view>
				</navigator>
			</view>
			<view class="free_grid_1">
				<navigator open-type="switchTab" url="/pages/cart/cart" hover-class="navigator-hover">
				<image class="img" mode='widthFix'  src="../../static/1.png"></image><view class="name">bbb</view>
				</navigator>
			</view><view class="free_grid_1">
				<navigator open-type="switchTab" url="/pages/cart/cart" hover-class="navigator-hover">
				<image class="img" mode='widthFix'  src="../../static/1.png"></image><view class="name">bbb</view>
				</navigator>
			</view><view class="free_grid_1">
				<navigator open-type="switchTab" url="/pages/cart/cart" hover-class="navigator-hover">
				<image class="img" mode='widthFix'  src="../../static/1.png"></image><view class="name">bbb</view>
				</navigator>
			</view><view class="free_grid_1">
				<navigator open-type="switchTab" url="/pages/cart/cart" hover-class="navigator-hover">
				<image class="img" mode='widthFix'  src="../../static/1.png"></image><view class="name">bbb</view>
				</navigator>
			</view><view class="free_grid_1">
				<navigator open-type="switchTab" url="/pages/cart/cart" hover-class="navigator-hover">
				<image class="img" mode='widthFix'  src="../../static/1.png"></image><view class="name">bbb</view>
				</navigator>
			</view><view class="free_grid_1">
				<navigator open-type="switchTab" url="/pages/cart/cart" hover-class="navigator-hover">
				<image class="img" mode='widthFix'  src="../../static/1.png"></image><view class="name">bbb</view>
				</navigator>
			</view>
		</view>
		<view class="uni-padding-wrap">
			<view class="uni-swiper-msg">
				<view class="uni-swiper-msg-icon">
					<image src="https://img-cdn-qiniu.dcloud.net.cn/uniapp/images/uni@2x.png" mode="widthFix"></image>
				</view>
				<swiper vertical="true" autoplay="true" circular="true" interval="3000">
					<swiper-item v-for="(item, index) in msg" :key="index">
						<navigator>{{item}}</navigator>
					</swiper-item>
				</swiper>
			</view>
		</view>
	</view>
</template>

<script>
	import uniNavBar from "@/components/uni-nav-bar.vue"
	import uniIcon from "@/components/uni-icon.vue"
	export default {
		components: {uniNavBar,uniIcon},
		data() {
			return {
				background: ['color1', 'color2', 'color3'],
				indicatorDots: true, 
				autoplay: true,
				interval: 2000,
				duration: 500,
				msg : [
					'uni-app行业峰会频频亮相，开发者反响热烈',
					'DCloud完成B2轮融资，uni-app震撼发布',
					'36氪热文榜推荐、CSDN公号推荐 DCloud CEO文章'
				]
			};
		},
		created(){
			uni.showToast({
				title: '标题',
				duration: 2000
			});
		},
		methods:{
			clickLeft() {
				uni.showToast({
					title: '左侧按钮'
				})
			},
			search() {
				uni.showToast({
					title: '搜索'
				})
			},
			showCity() {
				uni.showToast({
					title: '选择城市'
				})
			},
			scan() {
				uni.showToast({
					title: '扫码'
				})
			},
			confirm() {
				uni.showToast({
					title: '搜索'
				})
			}
		}
	}
</script>

<style>
	.free_grid {
		width:100%;
		overflow: auto;
		display: flex;
		flex-direction:row;
		flex-wrap: wrap;
		flex-grow: ;
	}
	.free_grid_1{
		width: 25%;
		text-align: center;
		margin-bottom:5px;
	}
	.free_grid_1 .img{
		width:50%;
	}
	.free_grid_1 .name{
		margin-top:-5px;
	}
	
	.input-view {
		width: 92%;
		display: flex;
		background-color: #e7e7e7;
		height: 30px;
		border-radius: 15px;
		padding: 0 4%;
		flex-wrap:nowrap;
		margin:7px 0;
		line-height:30px;
	}
	
	.input-view .uni-icon{
		line-height:30px !important;
	}
	
	.input-view .input {
		height:30px;
		line-height:30px;
		width:94%;
		padding: 0 3%;
	}
	.navbarFreeIcon{
		width:34px;
		font-size:12px;
		text-align: center;
	}
	
</style>
