<!-- 我的个人中心 -->
<template>
	<view class="my_content">
		<view class="my_login">
			<view class="user_icon">
				<image src="../../static/images/icon/icon_user.jpg" mode=""></image>
			</view>
			<text class="user_name">用户登录</text>
			<text class="iconfont icon_triangle">&#xe630;</text>
		</view>
		<view class="my_wallet">
			<view>
				<text>--</text>
				<text>账户余额</text>
			</view>
			<view>
				<text>--</text>
				<text>咖啡钱包</text>
			</view>		
			<view>
				<text>--</text>
				<text>优惠券</text>
			</view>
			<view>
				<text>--</text>
				<text>礼品卡</text>
			</view>
		</view>
		<view class="my_list">
			<view>
				<text class="iconfont icon_item">&#xe635;</text>
				<text class="text">收货地址</text>
				<text class="iconfont icon_triangle">&#xe630;</text>
			</view>
			<view>
				<text class="iconfont icon_item">&#xe63d;</text>
				<text class="text">兑换优惠</text>
				<text class="iconfont icon_triangle">&#xe630;</text>
			</view>
			<view>
				<text class="iconfont icon_item">&#xe6b8;</text>
				<text class="text">发票管理</text>
				<text class="iconfont icon_triangle">&#xe630;</text>
			</view>
			<view>
				<text class="iconfont icon_item">&#xe604;</text>
				<text class="text">客户服务</text>
				<text class="iconfont icon_triangle">&#xe630;</text>
			</view>
		</view>
		<view class="my_banner">
			<image src="../../static/images/img_my_bn_03.jpg" mode=""></image>
		</view>
	</view>
</template>

<script>
</script>

<style lang="less">
	@import '../../common/iconfont.css';
	.icon_triangle{
		font-size: 30rpx;
		color: #d1d0ce;
		font-weight: bold;
	}
	.my_content{
		width: 100%;
		padding: 0 30rpx;
		box-sizing: border-box;
		background:url(../../static/images/bg_login.jpg)no-repeat;
		background-size:100% 270rpx;
	}
	.my_login{
		display: flex;
		justify-content: space-between;
		align-items: center;
		width: 100%;
		height: 270rpx;
		.user_icon{
			width: 100rpx;
			height: 100rpx;
			border-radius: 50%;
			overflow:hidden;
			border: 2rpx solid #fff;
			box-shadow:0rpx 0rpx 5rpx 5rpx rgba(0,0,0,0.05);
			image{
				width: 100%;
				height: 100%;
			}
		}
		.user_name{
			flex: 1;
			padding-left: 30rpx;
			box-sizing: border-box;
			font-size: 30rpx;
			color: #333;
		}
	}
	.my_wallet{
		display: flex;
		align-items: center;
		width: 100%;
		height: 140rpx;
		border-radius:7rpx;
		box-shadow:0rpx 0rpx 5rpx 5rpx rgba(0,0,0,0.05);
		>view{
			flex: 1;
			>text{
				display: block;
				text-align: center;
				&:nth-child(1){
					font-size: 24rpx;
					color: #333;
				}
				&:nth-child(2){
					font-size: 24rpx;
					color: #888;
					margin-top: 15rpx;
				}
			}
		}
	}
	.my_list{
		width: 100%;
		margin-top: 10rpx;
		>view{
			display: flex;
			align-items: center;
			width: 100%;
			height: 100rpx;
			>.icon_item{
				width: 54rpx;
				font-size: 40rpx;
				color: #d1d0d5;
				font-weight: bold;
				text-align: center;
				margin-right: 20rpx;
			}
			.text{
				flex: 1;
				font-size: 30rpx;
				color: #333;
			}
		}
	}
	.my_banner{
		width: 100%;
		height: 204rpx;
		margin-top:46rpx;
		border-radius:10rpx;
		overflow:hidden;
		>image{
			width: 100%;
			height: 100%;
		}
	}
</style>
