<template>
	<view class="page">
		<!-- 搜索栏 -->
		<view class="search-box" style="padding: 20rpx; box-sizing: border-box;position: relative;">
			<image src="../../static/search.png" mode="" style="position: absolute;height: 30rpx;width: 30rpx;left: 40rpx;top: 40rpx;"></image>
			 <input style="height: 66rpx; background-color: #ffffff;border-radius: 30rpx; font-size: 26rpx; padding-left: 50rpx;" class="uni-input" confirm-type="search" placeholder="请输入商品名称" />
		</view>
		
		<view class="regory" style="display: flex;">
			<view class="regory-left">
				<view :class="active==index? 'active':''" v-for="(item,index) in 5" :key="index" @click="select(index)">
					<view style="margin-left: 10rpx;">全部</view>
				</view>
			</view>
			
			<scroll-view scroll-y="true" class="regory-right" >
				<view class="product-item" v-for="item in 10">
					<view>
						<image src="../../static/test.jpg" mode="" style="height: 100%;width: 100%;"></image>
					</view>
					<view>非转基因食用油</view>
					<view>￥80.00+250同呗 +800积分</view>
				</view>
				<view></view>
			</scroll-view>
		</view>
		
	</view>
</template>

<script>
	export default{
		data(){
			return{
				active:0
			}
		},
		methods:{
			select(e){
				console.log(e)
				this.active = e
			}
		}
	}
</script>

<style>
	.search-box{
		width:750rpx;
		height:100rpx;
		background:rgba(225,180,95,1);
	}
	
	.regory{
		height: calc(100% - 100rpx);
		width: 100%;
		margin-top: 26rpx;
	}
	
	/* 左边列表 */
	.regory-left{
		width: 180rpx;
		height: 100%;
	}
	
	.regory-left>view{
		height: 60rpx;
		width: 100%;
		padding-left: 18rpx;
		line-height: 60rpx;
		color: #999999;
		box-sizing: border-box;
		margin-top: 20rpx;
	}
	
	/* 右边order */
	.regory-right{
		height: 100%;
		
	}
	
	.product-item{
		width: 260rpx;
		display: inline-block;
		margin-left: 29rpx;
		margin-top: 54rpx;
	}
	
	.product-item:nth-child(1){
		margin-top: 0rpx;
	}
	.product-item:nth-child(2){
		margin-top: 0rpx;
	}
	
	
	.product-item>view:nth-child(1){
		width: 258rpx;
		height: 200rpx;
	}
	
	.product-item>view:nth-child(2){
		color: #333333;
		font-size: 30rpx;
		font-weight:700;
		margin-top: 32rpx;
	}
	
	.product-item>view:nth-child(3){
		color: #D21313;
		font-size: 26rpx;
		margin-top: 23rpx;
	}
	
	.active{
		border-left: 6rpx solid #00FF00;
		color: #333333!important;
		font-weight:700;
	}	
</style>
