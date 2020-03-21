<template>
	<view class="page">
		<view class="store-bg"></view>
		
		<view class="storeinfo-wrap">
			<view><image src="../../static/test.jpg" mode="" style="height: 100%;width: 100%;border-radius: 50%;"></image></view>
			<view>
				<view>东南饺子店</view>
				<view style="color: #666666;font-size: 26rpx;">北京市东城区白桥大街22号</view>
			</view>
			<view>
				<view style="width: 32rpx;height: 32rpx;margin: auto;"><image src="../../static/home/baihuo.png" mode="" style="height: 100%;width: 100%;"></image></view>
				<view style="font-size:22rpx;color: #666666;">50收藏</view>
			</view>
		</view>
		
		<!-- 商品列表 -->
		<view class="product-wrap">
			<view style="padding-bottom: 20rpx;">商品列表</view>
			<view v-for="item in 3" class="product-item">
				<view><image src="../../static/test.jpg" mode="" style="height: 100%;width: 100%;border-radius: 10rpx;"></image></view>
				<view>
					<view>阿波仔脆鸭肠跪卤香辣味*250g  <text style="margin-left: 20rpx;">约11袋</text></view>
					<view style="color: #f72929;">￥58.00 <text style="color: #999999;;margin-left: 50rpx;">500个起批</text> </view>
				</view>
			</view>
		</view>
		
		<view class="fx-bottom">
			<view>一键导航</view>
			<view>联系商家</view>
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
	.store-bg{
		height: 567rpx;
		background-image: url('https://ss1.bdstatic.com/70cFuXSh_Q1YnxGkpoWK1HF6hhy/it/u=3656355555,694789608&fm=26&gp=0.jpg');
		background-size: 100% 100%;
	}
	
	.storeinfo-wrap{
		display: flex;
		margin: 0rpx 30rpx;
		box-sizing: border-box;
		height: 100rpx;
		justify-content: space-between;
	}
	
	.storeinfo-wrap>view:nth-child(1){
		width: 142rpx;
		height: 142rpx;
		margin-top: -71rpx;
	}
	.storeinfo-wrap>view:nth-child(2){
		font-size: 30rpx;
		color: #333333;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		margin-left: -90rpx;
	}
	.storeinfo-wrap>view:nth-child(3){
		display: flex;
		flex-direction: column;
		justify-content: space-between;
	}
	
	/* 商品列表 */
	.product-wrap{
		margin: 10rpx 33rpx 0rpx;
		box-sizing: border-box;
		font-size: 26rpx;
		padding-bottom: 130rpx;
	}
	.product-item{
		height: 135rpx;
		display: flex;
	}
	.product-item>view:nth-child(1){
		width: 116rpx;
		height: 116rpx;
	}
	.product-item>view:nth-child(2){
		display: flex;
		flex-direction: column;
		justify-content: space-around;
		margin-left: 30rpx;
	}
	
	
	/* 底部 */
	.fx-bottom{
		height: 110rpx;
		width: 100%;
		display: flex;
		justify-content: space-between;
		font-size: 32rpx;
		color: #FFFFFF;
		position: fixed;
		bottom: 0;
	}
	
	.fx-bottom>view:nth-child(1){
		background: #e1b45f;
		width: 280rpx;
		display: flex;
		justify-content: center;
		align-items: center;
	}
	.fx-bottom>view:nth-child(2){
		background: #f92241;
		width: 470rpx;
		display: flex;
		justify-content: center;
		align-items: center;
	}
</style>
