<!-- 列表项 -->
<template>
	<view class="list_item">
		<view class="text">
			<text>{{text}}<text class="discount" v-if="tips!=''">{{tips}}</text></text>
			<text>{{englishText}}</text>
		</view>
		<view class="icon">
			<image class="img" :src="imgUrl"></image>
		</view>
	</view>
</template>

<script>
	
	export default {
		components: {
			
		},
		props:{
			text:{
				type:String,
				default:''
			},
			englishText:{
				type:String,
				default:''
			},
			tips:{
				type:String,
				default:''
			},
			imgUrl:{
				type:String,
				default:''
			},
		},
		data() {
			return {

			}
		},
		onLoad() {

		},
		methods: {
			
		}
	}
</script>


<style lang="less">
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
					background-color: #df8206;
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
			border: 3rpx solid #ccc;
			display:flex;
			justify-content:center;
			align-items: center;
			>image{
				width: 50rpx;
				height: 50rpx;
			}
		}
	}
</style>