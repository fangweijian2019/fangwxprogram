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

</style>
