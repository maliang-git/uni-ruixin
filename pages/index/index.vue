<!-- 首页 -->
<template>
	<view class="content">
		<bannerSwiper mode='default'></bannerSwiper>
		<view class="home_content">
			<view class="list_item first_item" v-for="(item,index) in homeList" :key="index">
				<view class="text">
					<text>{{item.title}}<text class="discount" v-if="item.discountInfo!=''">{{item.discountInfo}}</text></text>
					<text>{{item.englishTitle}}</text>
				</view>
				<view class="icon">
					<image class="img" :src="item.iconUrl"></image>
				</view>
			</view>
			<view class="btm_bn">
				<image src="/static/images/img_home_bn_03.jpg" ></image>
			</view>
		</view>
	</view>
</template> 

<script>
	import bannerSwiper from "@/components/my-components/my-swiper/bn-swiper.vue"
	export default {
		components: {
			bannerSwiper,
		},
		data() {
			return{
				homeList:[{
					title:"现在下单",
					englishTitle:"ORDER NOW",
					discountInfo:"",
					iconUrl:"/static/images/icon/icon_cofi.png"
				},{
					title:"咖啡钱包",
					englishTitle:"COFFEE WALLET",
					discountInfo:"充2赠1",
					iconUrl:"/static/images/icon/icon_yhq.png"
				},{
					title:"送他咖啡",
					englishTitle:"SEND COFFEE",
					discountInfo:"",
					iconUrl:"/static/images/icon/icon_liwu.png"
				}],
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style lang="less">
	.content{
		width: 100%;
	}
	.uni-status-bar {
		height: 0 !important;
	}
	.home_content{
		width: 100%;
		padding: 0 50rpx;
		box-sizing: border-box;
		.first_item{
			border-top: none!important;
		}
		.list_item{
			display: flex;
			justify-content: space-between;
			align-items: center;
			width: 100%;
			height: 140rpx;
			border-top:2rpx solid #eeee;
			.text{
				display:flex;
				flex-direction: column;
				&>text:nth-child(1){
					display: flex;
					font-weight: bold;
					font-size: 32rpx;
					color:#333;
					.discount{
						padding: 2rpx 8rpx;
						box-sizing: border-box;
						border-radius: 4rpx;
						background-color: #db7028;
						font-size: 20rpx;
						font-weight: bold;
						color: #fff;
						margin-left: 12rpx;
						vertical-align: middle;
					}
				}
				&>text:nth-child(2){
					font-size: 20rpx;
					color: #666;
				}
			}
			>.icon{
				width: 70rpx;
				height: 70rpx;
				border-radius: 50%;
				border: 3rpx solid #c5bcb3;
				display:flex;
				justify-content:center;
				align-items: center;
				>image{
					width: 50rpx;
					height: 50rpx;
				}
			}
		}
		.btm_bn{
			width: 100%;
			height: 112rpx;
			overflow:hidden;
			border-radius: 10rpx;
			margin-top:10rpx;
			>image{
				width: 100%;
				height: 100%;
			}
		}
	}
</style>
