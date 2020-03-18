<!-- banner swiper -->
<template>
	<view>
		<swiper class="swiper" :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval" :duration="duration" indicator-color="rgba(255, 255,255,0.3)" indicator-active-color="#fff">
			<swiper-item v-for="(item,index) in info" :key="index">
				<view class="img">
					<image class="img" :src="item.url"></image>
				</view>
			</swiper-item>
		</swiper>
	</view>
</template>

<script>
	
	export default {
		components: {
			
		},
		props:['mode'],
		data() {
			return {
				indicatorDots: true,
				autoplay: true,
				interval: 5000,
				duration: 500,
				info: [{
					url: '/static/images/img_home_bn_01.jpg'
				},{
					url: '/static/images/img_home_bn_02.jpg'
				}],
			}
		},
		onLoad() {

		},
		methods: {
			
		}
	}
</script>


<style>
	.swiper{
		width: 100%;
		height: 500rpx;
	}
	.img{
		width: 100%;
		height: 500rpx;
	}
	.uni-swiper-dot{
		background-color: #fff!important;
	}
</style>
