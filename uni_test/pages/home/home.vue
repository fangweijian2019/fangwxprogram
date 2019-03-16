<template>
	<view>
		<uni-nav-bar left-icon="back" left-text="返回" right-text="菜单" title="导航栏组件"></uni-nav-bar>
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
	export default {
		components: {uniNavBar},
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
</style>
