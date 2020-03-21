<template>
	<view class="page">
		<!-- 地址信息 -->
		<view class="address-wrap">
			<view><image src="../../static/home/baihuo.png" style="width: 48rpx;height: 52rpx;" mode=""></image></view>
			<view>
				<view><text>留煌</text>  15360664445</view>
				<view>广东省广州市天河区天河大道152号弓凛二路易安马大厦520</view>
			</view>
			<view>></view>
		</view>
		
		<!-- 商品信息 -->
		<view class="product-wrap">
			<h1>商品详情</h1>
			<view>
				<view><image src="../../static/test.jpg" style="height: 140rpx;width: 140rpx;" mode=""></image></view>
				<view style="width: 492rpx;display: flex;flex-direction: column;justify-content: space-between;">
					<view>Ayuko 时髦气质毛呢外套 加棉可脱卸呢大衣</view>
					<view style="display: flex;justify-content: space-between;">
						<view>红色</view>
						<view>-2+</view>
					</view>
				</view>
			</view>
			
			<view>
				<view>单价</view>
				<view style="margin-left: 80rpx;color: #f92f3b;">￥6000.00+50同呗</view>
			</view>
			
			<view>
				<view>赠送</view>
				<view style="margin-left: 80rpx;color: #f92f3b;">￥6000积分  5000同呗  3000消呗</view>
			</view>
			
			<view>
				<view>备注</view>
				<view style="margin-left: 80rpx;"><input type="text" placeholder="请填写你的备注" /></view>
			</view>
		</view>
		
		
		<!-- 合计 -->
		<view class="sum-wrap">
			<view>
				<view>合计</view>
				<view>￥60000.00+500同呗</view>
			</view>
			<view>账户同呗余额:<text style="color: #f92f3b;">5272</text></view>
		</view>
		
		<!-- 支付 -->
		<view style="margin: 20rpx; box-sizing: border-box;"><button type="primary">微信支付</button></view>
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
	/* 商品信息 */
	.product-wrap{
		margin: 20rpx 20rpx 0rpx;
		background-color: #ffffff;
		border-radius: 10px;
		padding: 35rpx 20rpx;
		box-sizing: border-box;
	}
	
	.product-wrap>view:nth-child(1){
		
	}
	.product-wrap>view:nth-child(2){
		display: flex;
		justify-content: space-between;
		margin-top: 45rpx;
	}
	.product-wrap>view:nth-child(3){
		display: flex;
		margin-top: 45rpx;
	}
	.product-wrap>view:nth-child(4){
		display: flex;
		margin-top: 45rpx;
	}
	.product-wrap>view:nth-child(5){
		display: flex;
		margin-top: 45rpx;
	}
	
	
	/* 地址信息 */
	.address-wrap{
		margin: 20rpx 20rpx 0rpx;
		background-color: #ffffff;
		border-radius: 10px;
		height: 189rpx;
		display: flex;
		justify-content: space-between;
	}
	
	.address-wrap>view:nth-child(1){
		display: flex;
		justify-content: center;
		align-items: center;
		width: 150rpx;
	}
	.address-wrap>view:nth-child(2){
		width: 460rpx;
		padding: 32rpx 0rpx;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		font-size: 28rpx;
		color: #999999;
	}
	.address-wrap>view:nth-child(3){
		display: flex;
		justify-content: center;
		align-items: center;
		width: 90rpx;
	}
	
	/* 合计 */
	.sum-wrap{
		margin: 20rpx 20rpx 0rpx;
		border-radius: 10px;
		background-color: #ffffff;
		padding: 35rpx 20rpx;
		box-sizing: border-box;
	}
	
	.sum-wrap>view:nth-child(1){
		display: flex;
		justify-content: space-between;
	}
	.sum-wrap>view:nth-child(2){
		display: flex;
		justify-content: flex-end;
		margin-top: 30rpx;
	}
</style>
