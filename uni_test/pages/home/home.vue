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
			<view class="free_grid_1"><image class="img" mode='widthFix'  src="../../static/1.png"></image><view class="name">bbb</view></view>
			<view class="free_grid_1"><image class="img" mode='widthFix'  src="../../static/1.png"></image><view class="name">bbb</view></view>
			<view class="free_grid_1"><image class="img" mode='widthFix'  src="../../static/1.png"></image><view class="name">bbb</view></view>
			<view class="free_grid_1"><image class="img" mode='widthFix'  src="../../static/1.png"></image><view class="name">bbb</view></view>
			<view class="free_grid_1"><image class="img" mode='widthFix'  src="../../static/1.png"></image><view class="name">bbb</view></view>
			<view class="free_grid_1"><image class="img" mode='widthFix'  src="../../static/1.png"></image><view class="name">bbb</view></view>
			<view class="free_grid_1"><image class="img" mode='widthFix'  src="../../static/1.png"></image><view class="name">bbb</view></view>
			<view class="free_grid_1"><image class="img" mode='widthFix'  src="../../static/1.png"></image><view class="name">bbb</view></view>
			
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
				duration: 500
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
