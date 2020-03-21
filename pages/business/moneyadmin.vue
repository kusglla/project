<template>
	<view class="page">
		<view class="moneysum-wrap">
			<view>
				<view>累计获得奖励金</view>
				<view style="font-size: 32rpx;color: #F11F1F;margin-top: 30rpx;">￥168.88</view>
			</view>
			<view>
				提现
			</view>
		</view>
		
		<view style="height: 10rpx;width: 100%;background: #EEEEEE;"></view>
		
		<!-- 日期交易流水 -->
		<view class="daymoney-wrap">
			<view>2020-02-02 至 2020-02-02  查询</view>
			
			<view>
				<view style="padding: 0rpx 60rpx;">
					<view style="font-size: 38rpx;color: #F11F1F;margin-bottom: 30rpx;">1688.88</view>
					<view>交易流水</view>
				</view>
				<view style="height: 60rpx;width: 2rpx;background:rgba(51,51,51,1);"></view>
				<view style="padding: 0rpx 60rpx;">
					<view style="font-size: 38rpx;color: #F11F1F;margin-bottom: 30rpx;">1688.88</view>
					<view>奖励金</view>
				</view>
			</view>
		</view>
		
		<!-- 线下消费项 -->
		<view class="cutmoney-wrap">
			<view class="cutmoney-item" v-for="item in 3">
				<view>
					<view>线下消费</view>
					<view>2019-05-04 20:20:00</view>
				</view>
				
				<view>
					<view>￥168丨奖励金</view>
					<view style="display: flex;justify-content: center;align-items: center;">小黑 <image src="../../static/test.jpg" style="width: 50rpx;height: 50rpx;border-radius: 50%;" mode=""></image></view>
				</view>
				
				<view>
					<view><image src="../../static/test.jpg" style="height: 78rpx;width: 78rpx;" mode=""></image></view>
					<view>
						<view>商家名称</view>
						<view>￥168</view>
					</view>
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
			
		}
	}
</script>

<style>
	/* 累计奖励 */
	.moneysum-wrap{
		background: #FFFFFF;
		padding: 35rpx 35rpx 45rpx;
		display: flex;
		justify-content: space-between;
	}
	
	.moneysum-wrap>view:nth-child(1){}
	.moneysum-wrap>view:nth-child(2){
		display: flex;
		align-items: center;
	}
	
	/* 查询账目日期 */
	.daymoney-wrap{
		background-color: #FFFFFF;
		padding: 25rpx 40rpx 50rpx;
	}
	
	.daymoney-wrap>view:nth-child(1){}
	.daymoney-wrap>view:nth-child(2){
		display: flex;
		justify-content: center;
		margin-top: 65rpx;
		font-size: 28rpx;
		color: #333333;
		text-align: center;
	}
	
	/* 线下消费 */
	.cutmoney-wrap{
		box-sizing: border-box;
		background: #FFFFFF;
	}
	
	.cutmoney-item{
		border-top: 1px solid #EEEEEE;
		padding: 40rpx 40rpx 55rpx;
	}
	
	.cutmoney-item>view:nth-child(1){
		display: flex;
		justify-content: space-between;
	}
	.cutmoney-item>view:nth-child(2){
		display: flex;
		justify-content: space-between;
		margin-top: 25rpx;
	}
	.cutmoney-item>view:nth-child(3){
		width: 100%;
		height: 115rpx;
		box-sizing: border-box;
		background: #F1F1F1;
		padding: 20rpx 25rpx;
		display: flex;
		margin-top: 35rpx;
	}
</style>
