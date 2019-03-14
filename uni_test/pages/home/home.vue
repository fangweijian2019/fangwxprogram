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
			 <image style="width: 200px; height: 200px; background-color: #eeeeee;" src="../../static/cart.png"></image>
		</swiper>
		<uni-grid :data="[
			{image:'https://img-cdn-qiniu.dcloud.net.cn/img/shu.png',text:'圣诞树'},
			{image:'https://img-cdn-qiniu.dcloud.net.cn/img/lindang.png',text:'铃铛'},
			{image:'https://img-cdn-qiniu.dcloud.net.cn/img/laoren.png',text:'圣诞老人'},
			{image:'https://img-cdn-qiniu.dcloud.net.cn/img/liwu.png',text:'礼物'},
			{image:'https://img-cdn-qiniu.dcloud.net.cn/img/maozi.png',text:'帽子'},
			{image:'https://img-cdn-qiniu.dcloud.net.cn/img/shoutao.png',text:'手套'}]" 
			show-border="false">
		</uni-grid>
	</view>
</template>

<script>
	import uniNavBar from "@/components/uni-nav-bar.vue"
	import uniGrid from "@/components/uni-grid/uni-grid.vue"

	export default {
		components: {uniNavBar,uniGrid},
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
