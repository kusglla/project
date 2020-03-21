<template>
	<view class="page" style="color: #333333;">
		<!-- 订单状态栏 -->
		<view class="status-wrap">
			<view @click="tabType(0)" :class="[type==0? 'active':'']">全部</view>
			<view @click="tabType(1)" :class="[type==1? 'active':'']">待支付</view>
			<view @click="tabType(2)" :class="[type==2? 'active':'']">代发货</view>
			<view @click="tabType(3)" :class="[type==3? 'active':'']">待收货</view>
			<view @click="tabType(4)" :class="[type==4? 'active':'']">已完成</view>
		</view>
		
		<!-- 订单列表 -->
		<view class="order-wrap">
			<view class="order-item" v-for="item in 4" @click="onDetail()">
				<view>
					<view>订单号: 2384759021512</view>
					<view style="color: #eb0029;">待支付</view>
				</view>
				<view style="border-bottom: 1rpx solid #eeeeee; padding: 30rpx 0rpx;">
					<view class="left"><image src="../../static/test.jpg" style="height: 100%;width: 100%;" mode=""></image></view>
					<view class="right">
						<view>夏季女装甜美小裙子</view>
						<view>规格1</view>
						<view>
							<view>￥10.00+100同呗</view>
							<view>×1</view>
						</view>
					</view>
				</view>
				
				<view style="display: flex;justify-content: flex-end;padding: 22rpx 0rpx;">
					<view class="btn-bg" style="margin-right: 27rpx;">取消订单</view>
					<view class="btn-bg">立即支付</view>
				</view>
			</view>
		</view>
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				type:0
			}
		},
		methods: {
			tabType(e){
				this.type = e
			},
			onDetail(){
				uni.navigateTo({
					url:'../order/detail'
				})
			}
		}
	}
</script>

<style>
	.status-wrap{
		display: flex;
		justify-content: space-between;
		padding: 0rpx 20rpx;
		box-sizing: border-box;
	}
	
	.status-wrap>view{
		padding: 20rpx 10rpx;
		font-size: 32rpx;
	}
	
	.active{
		border-bottom: 4rpx solid #f3be5b;;
		color: #f3be5b;
	}
	
	/* 订单列表 */
	.order-wrap{
		padding: 0rpx 20rpx;
		box-sizing: border-box;
	}
	
	.order-item{
		padding: 0rpx 30rpx;
		box-sizing: border-box;
		padding: 20rpx;
		box-sizing: border-box;
		margin-top: 30rpx;
		background-color: #ffffff;
		box-shadow: 0px 0px 13px 0px rgba(1, 1, 1, 0.09);
		border-radius: 10px;
	}
	
	.order-item>view:nth-child(1){
		font-size: 26rpx;
		color: #333333;
		font-weight: bold;
		display: flex;
		justify-content: space-between;
	}
	.order-item>view:nth-child(2){
		display: flex;
	}
	
	.order-item .left{
		height: 158rpx;
		width: 158rpx;
	}
	.order-item .right{
		margin-left: 40rpx;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
	}
	
	.order-item .right>view:nth-child(1){
		letter-spacing: 2rpx;
		color: #333333;
	}
	.order-item .right>view:nth-child(2){
		letter-spacing: 1rpx;
		color: #999999;
	}
	.order-item .right>view:nth-child(3){
		display: flex;
		letter-spacing: 2rpx;
		color: #eb0029;
	}
	
	.btn-bg{
		width: 139rpx;
		height: 57rpx;
		border-radius: 10rpx;
		border: solid 1rpx #cccccc;
		font-size: 26rpx;
		color: #999999;
		display: flex;
		justify-content: center;
		align-items: center;
	}
</style>
