<template>
	<view class="page">
		<view class="search-box" style="padding: 20rpx; box-sizing: border-box;position: relative;">
			<image src="../../static/search.png" mode="" style="position: absolute;height: 30rpx;width: 30rpx;left: 40rpx;top: 40rpx;"></image>
			 <input style="height: 66rpx; background-color: #ffffff;border-radius: 30rpx; font-size: 26rpx; padding-left: 50rpx;" class="uni-input" confirm-type="search" placeholder="请输入商品名称" />
		</view>
		
		<view class="product-wrap">
			<view class="product-item" v-for="item in 4">
				<view><image src="../../static/test.jpg" mode="" style="height: 223rpx;width: 308rpx;border-radius: 10rpx;"></image></view>
				<view>嬉游记原创 休闲两面穿外套 宽松显瘦大衣女款</view>
				<view>￥1500</view>
				<view>800积分</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default{
		data(){
			return{
				
			}
		},
	}
</script>

<style>
	.product-wrap{
		display: flex;
		flex-wrap: wrap;
		justify-content: space-between;
		margin: 0rpx 40rpx;
		box-sizing: border-box;
	}
	
	.product-item{
		width: 310rpx;
		margin-top: 41rpx;
	}
	
	.product-item>view:nth-child(1){
		width: 308rpx;
		height: 223rpx;
		border-radius: 10rpx;
	}
	.product-item>view:nth-child(2){
		font-size:28rpx;
		font-weight:700;
		color:rgba(51,51,51,1);
		margin-top: 25rpx;
	}
	.product-item>view:nth-child(3){
		font-size:32rpx;
		font-weight:700;
		color:rgba(251,70,50,1);
		margin-top: 25rpx;
	}
	.product-item>view:nth-child(4){
		font-size:24rpx;
		font-weight:700;
		color:rgba(153,153,153,1);
		margin-top: 7rpx;
	}
	
	/* 搜索栏 */
	.search-box{
		width:750rpx;
		height:101rpx;
		background:rgba(225,180,95,1);
	}
</style>
