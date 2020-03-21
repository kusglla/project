<template>
	<view class="page">
		<view class="top-bg">
			
			<view class="content">
				<view>
					<view>待支付</view>
					<view style="margin-top: 26rpx; font-size: 26rpx;">2小时内未支付将自动取消订单</view>
				</view>
				<view>
					<image src="../../static/home/baihuo.png" style="height: 70rpx;width: 80rpx" mode=""></image>
				</view>
			</view>
			
		</view>
		
		<view class="line"></view>
		
		 <view class="producinfo-wrap">
			<view>商品信息</view>
			<view>
				<view class="left"><image src="../../static/test.jpg" style="height: 100%;width: 100%;border-radius: 10rpx;" mode=""></image></view>
				<view class="right">
					<view>甜美小香风超仙女连衣裙两件套秋冬新款两件套</view>
					<view>规格：红色</view>
					<view>
						<view>￥15.00+26通呗</view>
						<view>-2+</view>
					</view>
				</view>
			</view>
			<view>
				<view>运费</view>
				<view>免费</view>
			</view>
			<view>
				<view>总价</view>
				<view style="color: #f33b3b;">￥15.00+26同呗</view>
			</view>
			<view>
				<view>留言</view>
				<input type="text" value="" />
			</view>
		 </view>
		 
		 <!-- 订单信息 -->
		 <view class="orderinfo-wrap">
			<view>订单信息</view>
			<view>
				<view>订单编号:</view>
				<view  style="margin-left: 62rpx;">15263215521521</view>
			</view>
			<view>
				<view>下单时间:</view>
				<view style="margin-left: 62rpx;">2020-01-18  16:48:20</view>
			</view>
			<view>
				<view>收货地址:</view>
				<view  style="margin-left: 62rpx;">
					<view>林小姐  15360664445</view>
					<view>广东省广州市白云区嘉禾大厦均和路64号</view>
				</view>
				<view style="display: flex;justify-content: center;align-items: center;"> > </view>
			</view>
		 </view>
		
		<view class="bottom">
			<view>取消订单</view>
			<view>立即支付</view>
		</view>
	</view>
</template>

<script>
	export default{
		data(){
			return{
				
			}
		},
		methods:{
			
		}
	}
</script>

<style>
	/* 顶部 */
	.top-bg{
		width: 700rpx;
		margin: auto;
		padding: 43rpx 53rpx;
		box-sizing: border-box;
		height: 200rpx;
		background-image: linear-gradient(90deg, 
			#c78816 0%, 
			#e1ac56 0%, 
			#fbcf96 0%, 
			#e4ab4e 0%, 
			#cd8606 0%, 
			#ffca6b 68%, 
			#ce921f 100%, 
			#dca031 100%, 
			#e9ae43 100%), 
		linear-gradient(90deg, 
			#f986a7 0%, 
			#ff5083 100%);
		background-blend-mode: normal, 
			normal;
		border-radius: 10rpx;
		/* display: flex; */
	}
	
	.top-bg>.content{
		display: flex;
		justify-content: space-between;
		color: #FFFFFF;
	}
	.top-bg>.content>view:nth-child(1){
		font-size: 36rpx;
	}
	.top-bg>.content>view:nth-child(2){
		display: flex;
		justify-content: center;
		align-items: center;
	}
	
	.line{
		margin-top: 46rpx;
		border-top: 8rpx dashed skyblue;
	}
	
	/* 商品信息 */
	.producinfo-wrap{
		padding: 0rpx 33rpx;
		box-sizing: border-box;
		margin-top: 50rpx;
	}
	
	.producinfo-wrap>view:nth-child(1){}
	.producinfo-wrap>view:nth-child(2){
		padding: 50rpx 0rpx;
		display: flex;
	}
	.producinfo-wrap .left{
		width: 175rpx;
		height: 175rpx;
	}
	
	.producinfo-wrap .right{
		margin-left: 24rpx;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
	}
	
	.producinfo-wrap .right>view:nth-child(1){
		font-size: 28rpx;
		color: #333333;
	}
	.producinfo-wrap .right>view:nth-child(2){
		font-size: 24rpx;
		color: #999999;
	}
	.producinfo-wrap .right>view:nth-child(3){
		display: flex;
		justify-content: space-between;
		font-size: 28rpx;
		color: #f33b3b;
	}

	.producinfo-wrap>view:nth-child(3){
		display: flex;
		justify-content: space-between;
		font-size: 26rpx;
		color: #333333;
		margin-top: 20rpx;
	}
	.producinfo-wrap>view:nth-child(4){
		display: flex;
		justify-content: space-between;
		font-size: 26rpx;
		margin-top: 20rpx;
	}
	.producinfo-wrap>view:nth-child(5){
		font-size: 26rpx;
		margin-top: 20rpx;
	}
	
	/* 订单信息 */
	.orderinfo-wrap{
		padding: 0rpx 33rpx 200rpx;
		box-sizing: border-box;
		font-size: 26rpx;
		color: #666666;
	}
	.orderinfo-wrap>view:nth-child(1){
		font-size: 32rpx;
		color: #333333;
	}
	.orderinfo-wrap>view:nth-child(2){
		margin-top: 65rpx;
		display: flex;
	}
	.orderinfo-wrap>view:nth-child(3){
		margin-top: 32rpx;
		display: flex;
	}
	.orderinfo-wrap>view:nth-child(4){
		margin-top: 32rpx;
		display: flex;
	}
	
	
	
	/* 底部 */
	.bottom{
		position: fixed;
		bottom: 0;
		height: 110rpx;
		display: flex;
		font-size: 32rpx;
		width: 100%;
		color: #FFFFFF;
	}
	
	.bottom>view:nth-child(1){
		width: 50%;
		background: #323838;
		display: flex;
		justify-content: center;
		align-items: center;
	}
	.bottom>view:nth-child(2){
		width: 50%;
		background: #f3be5b;
		display: flex;
		justify-content: center;
		align-items: center;
	}
</style>
