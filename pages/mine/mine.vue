<template>
	<view class="mine-page">
		<view style="height: 300rpx;background: #E9AE43;">
			
		</view>
		
		<!-- 信息简介 -->
		<view style="width: 690rpx;height: 328rpx;border-radius: 20rpx; background: #FFFFFF;margin: -250rpx auto; 0rpx;padding: 25rpx 40rpx;box-sizing: border-box; box-shadow:0px 6px 27px 0px rgba(0, 0, 0, 0.08);">
			<view style="display: flex;border-bottom: 1rpx solid rgba(240,240,240,1);padding-bottom: 25rpx;">
				<view><image src="../../static/test.jpg" mode="" style="border-radius: 50%; height: 132rpx;width: 132rpx;"></image></view>
				<view style="color: #000000;margin-left: 40rpx;">
					<view>(*^▲^*)民</view>
					<view style="width: 236rpx;height: 40rpx; background: #000000;margin-top: 28rpx; font-size: 26rpx;text-align: center;line-height: 40rpx;border-radius: 20rpx;color: #FFFFFF;">未完成实名认证</view>
				</view>
			</view>
			<view style="display: flex;padding: 21rpx 0rpx;">
				<view style="width: 226rpx; text-align: center;">
					<view style="font-size: 40rpx;color: #333333;">23</view>
					<view style="font-size: 30rpx;color: #808080;">积分</view>
				</view>
				<view style="width: 226rpx; text-align: center;">
					<view style="font-size: 40rpx;color: #333333;">125</view>
					<view style="font-size: 30rpx;color: #808080;">好友</view>
				</view>
				<view style="width: 226rpx; text-align: center;">
					<view style="font-size: 40rpx;color: #333333;">120</view>
					<view style="font-size: 30rpx;color: #808080;">收藏</view>
				</view>
			</view>
		</view>
		
		<!-- 我的积分 -->
		<view style="margin-top: 300rpx;">
		</view>
		
		
		
		<!-- 我的订单 -->
		<view style="margin-top: 50rpx;">
			<!-- 标题 -->
			<view style="border-left: 6rpx solid #00FF00;">
				<view style="margin: 0rpx 36rpx;display: flex;justify-content: space-between;">
					<view style="font-size: 32rpx;color: #333333;">我的订单</view>
					<view style="font-size: 28rpx;color: #ACACAC;"  @click="onOrder">全部订单></view>
				</view>
			</view>
			
			<view style="display: flex;justify-content: space-around;color: #333333; margin-top: 33rpx;">
				<view v-for="item in 4">
					<view><image src="../../static/test.jpg" mode="" style="height: 80rpx;width: 80rpx;border-radius: 50%;"></image></view>
					<view>待发货</view>
				</view>
			</view>
		</view>
		
		
		<!-- 关于我的 -->
		<view style="margin-top: 50rpx;">
			<!-- 标题 -->
			<view style="border-left: 6rpx solid #00FF00;">
				<view style="margin: 0rpx 36rpx;display: flex;justify-content: space-between;">
					<view style="font-size: 32rpx;color: #333333;">关于我的</view>
				</view>
			</view>
			
			<view style="display: flex;justify-content: space-around;color: #333333; margin-top: 33rpx;">
				<view v-for="item in 3" style="width: 206.5rpx;height: 159rpx;border-radius: 10rpx; background: #01AAED;">
					我的钱包
				</view>
			</view>
		</view>
		
		<!-- 我的服务 -->
		<view style="margin-top: 50rpx;">
			<!-- 标题 -->
			<view style="border-left: 6rpx solid #00FF00;">
				<view style="margin: 0rpx 36rpx;display: flex;justify-content: space-between;">
					<view style="font-size: 32rpx;color: #333333;">我的服务</view>
				</view>
			</view>
			
			<view style="display: flex;flex-wrap: wrap;justify-content: space-around;color: #333333; padding: 0rpx 47rpx;margin-top: 33rpx;">
				<view v-for="item in 8" style="width: 140rpx;height: 130rpx; text-align: center; margin-top: 10rpx;">
					<view><image src="../../static/test.jpg" mode="" style="height: 54rpx;width: 56rpx;"></image></view>
					<view style="font: 28rpx; color: #666666;">我的商家</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			onOrder(){
				console.log('2')
				uni.navigateTo({
					url:'../order/order'
				})
			}
		}
	}
</script>

<style>
	.mine-page{
		color: #FDFCFA;
	}
</style>
