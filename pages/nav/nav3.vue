<template>
	<view class="page">
		<view class="top-bg">
			<view style="margin: 0rpx 66rpx; box-sizing: border-box;">
				<view v-for="(item,index) in robtime" :key="index" @click="selectTime(index)" :class="[index==activetime? 'active':'']">{{item}}</view>
			</view>
		</view>
		
		<!-- 抢购列表 -->
		<view class="rob-wrap">
			<view v-for="item in 3">
				<view><image src="../../static/test.jpg" mode="" style="width: 100%;height: 100%;border-radius: 10rpx;"></image></view>
				<view>嬉游记原创瘦大衣女中...</view>
				<view>500通呗</view>
			</view>
		</view>
		
		<!-- 搜索栏 -->
		<view class="search-box" style="padding: 20rpx; box-sizing: border-box;position: relative;">
			<image src="../../static/search.png" mode="" style="position: absolute;height: 30rpx;width: 30rpx;left: 40rpx;top: 40rpx;"></image>
			 <input style="height: 66rpx; background-color: #ffffff;border-radius: 30rpx; font-size: 26rpx; padding-left: 50rpx;" class="uni-input" confirm-type="search" placeholder="请输入商品名称" />
		</view>
		
		<!-- 精品闪抢 -->
		<view class="good-buy">
			<view class="goodbuy-title">
				<view></view>
				<view>精品闪购物</view>
				<view>更多></view>
			</view>
			
			<view class="product-list">
				<view v-for="item in 4" class="product-item">
					<view><image src="../../static/test.jpg" mode="" style="width: 308rpx;height: 223rpx;border-radius: 10rpx;"></image></view>
					<view>嬉游记原创 休闲两面穿外套 宽松显瘦大衣女款</view>
					<view>￥1500</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default{
		data(){
			return {
				robtime:['10:00','12:00','18:00'],
				activetime:0
			}
		},
		methods:{
			selectTime(e){
				this.activetime=e
				console.log(e)
			}
		}
	}
</script>

<style>
	.top-bg{
		width: 100%;
		height:155rpx;
		background:linear-gradient(90deg,rgba(233,174,67,1),rgba(206,146,32,1),rgba(255,203,107,1),rgba(205,134,6,1),rgba(205,134,6,1),rgba(251,207,150,1),rgba(199,136,22,1));
		padding-top: 46rpx;
	}
	.top-bg>view{
		display: flex;
		justify-content: space-between;
	}
	
	/* 抢购列表 */
	.rob-wrap{
		margin: -80rpx 22rpx 0rpx;
		box-sizing: border-box;
		height:412rpx;
		background:rgba(255,255,255,1);
		padding: 40rpx 40rpx 60rpx;
		box-shadow:0px 3px 8px 0px rgba(35,24,21,0.09);
		border-radius:10px;
		display: flex;
		justify-content: space-between;
	}
	
	.rob-wrap>view{
		width: 177rpx;
	}
	
	.rob-wrap>view>view:nth-child(1){
		width: 177rpx;
		height: 177rpx;
		border-radius: 10rpx;
	}
	
	.rob-wrap>view>view:nth-child(2){
		font-size:28rpx;
		font-weight:700;
		color:rgba(51,51,51,1);
		margin-top: 34rpx;
	}
	
	.rob-wrap>view>view:nth-child(3){
		font-size:26rpx;
		font-weight:700;
		color:rgba(251,58,41,1);
	}
	
	
	.rob-product{
		height:412px;
		background:rgba(255,255,255,1);
		box-shadow:0px 3px 8px 0px rgba(35,24,21,0.09);
		border-radius:10px;
	}
	
	/* 导航栏 */
	.search-box{
		margin-top: 10rpx;
		width:750rpx;
		height:100rpx;
		background:rgba(225,180,95,1);
	}
	
	/* 精品闪购 */
	.good-buy{
		margin: 16rpx 22rpx 0rpx;
	}
	
	.goodbuy-title{
		height: 68rpx;
		display: flex;
		justify-content: space-between;
		align-items: flex-end;
	}
	
	.goodbuy-title>view:nth-child(1){
		width: 100rpx;
	}
	
	.goodbuy-title>view:nth-child(2){
		font-size:32rpx;
		font-weight:700;
		color:rgba(51,51,51,1);
	}
	
	.goodbuy-title>view:nth-child(3){
		width: 100rpx;
		font-size:24rpx;
		font-family:PingFang SC;
		font-weight:500;
		color:rgba(153,153,153,1);
	}
	
	.product-list{
		display: flex;
		justify-content: space-between;
		flex-wrap: wrap;
		margin: 0rpx 18rpx;
		padding-bottom: 40rpx;
	}
	
	.product-item{
		width: 308rpx;
		margin-top: 43rpx;
	}
	
	.product-item>view:nth-child(1){
		border-radius: 10rpx;
	}
	
	.product-item>view:nth-child(2){
		width: 100%;
		font-size:28rpx;
		font-weight:700;
		color:rgba(51,51,51,1);
	}
	
	.product-item>view:nth-child(3){
		font-size:32rpx;
		font-weight:700;
		color:rgba(251,70,50,1);
	}
	
	.active{
		color: #FB3A29!important;
	}
</style>
