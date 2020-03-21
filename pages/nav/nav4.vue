<template>
	<view class="page">
		<!-- 分类 -->
		<view class="buytype-wrap">
			<view v-for="(item,index) in nav2" :key="index" @click="onStore(index)" class="buy-item" style="display: flex;flex-direction: column;justify-content: center;align-items: center;">
				<view :class="[index==2? 'img-bg3':'',index==7? 'img-bg7':'']">
					<image :src="item.img" mode=""></image>
				</view>
				<view style="font-size: 24rpx;color: #333333;margin-top: 10rpx;">{{item.text}}</view>
			</view>
		</view>
		
		<view style="background-color: #f6fafb;height: 21rpx;"></view>
		
		<!-- 推荐批发商 -->
		<view class="recommend">
			<view>推荐批发商</view>
			<view>朝阳区建国门外大街22号</view>
		</view>
		
		<view class="order-wrap">
			<view class="order-item" v-for="item in 4">
				<view class="left"><image src="../../static/test.jpg" mode="" style="height: 100%;width: 100%;border-radius: 10rpx;"></image></view>
				<view class="right">
					<view>兴盛世家城北点</view>
					<view>百货</view>
					<view>北京市东城区白桥大街22号</view>
					<view>距离152米</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default{
		data() {
			return {
				nav2:[
					{text:'超市百货',img:'../../static/home/lanzi.png'},
					{text:'蔬菜水果',img:'../../static/home/shuiguo.png'},
					{text:'小吃门店',img:'../../static/home/meishi.png'},
					{text:'日用百货',img:'../../static/home/baihuo.png'},
					{text:'服饰专区',img:'../../static/home/qunzi.png'}
				]
			}
		},
		methods:{
			
		}
	}
</script>

<style>
	/* 购物分类 */
	.buytype-wrap{
		padding: 0rpx 30rpx;
		border-radius: 10rpx;
		background:rgba(255,255,255,1);
		display: flex;
		justify-content: space-between;
		flex-wrap: wrap;
	}
	
	.buytype-wrap image{
		width: 57rpx;
		height: 56rpx;
		margin-top: 10rpx
	}
	
	.buy-item{
		width: 125rpx;
		text-align: center;
		margin-top: 30rpx;
	}
	
	.img-bg3{
		height: 72rpx;
		width: 72rpx;
		border-radius: 50%;
		background: #FF7F3B;
		text-align: center;
	}
	
	.img-bg3>image{
		height: 39rpx;
		width: 32rpx;
		margin-top: 20rpx;
	}
	
	.img-bg7{
		width: 66rpx;
		height: 79rpx;
		text-align: center;
		background: url(../../static/home/tybg.png)no-repeat;
		background-size: 100% 100%;
	}
	.img-bg7>image{
		height: 38rpx;
		width: 35rpx;
		margin-top: 15rpx;
	}
	
	/* 推荐 */
	.recommend{
		margin-top: 85rpx;
		padding: 0rpx 30rpx;
		display: flex;
	}
	.recommend>view:nth-child(1){
		font-size: 32rpx;
		color: #333333;
	}
	.recommend>view:nth-child(2){
		display: flex;
		flex-direction: column;
		justify-content: flex-end;
		font-size: 24rpx;
		color: #999999;
		margin-left: 35rpx;
	}
	
	
	/* 列表 */
	.order-wrap{
		padding: 0rpx 30rpx;
		margin-top: 58rpx;
	}
	.order-item{
		display: flex;
		margin-top: 25rpx;
	}
	.order-item>.left{
		width: 243rpx;
		height: 195rpx;
		border-radius: 10rpx
	}
	.order-item>.right{
		margin-left: 36rpx;
	}
	.order-item>.right>view:nth-child(1){
		font-size: 28rpx;
		color: #333333;
	}
	.order-item>.right>view:nth-child(2){
		width: 85rpx;
		height: 42rpx;
		border-radius: 10rpx;
		border: solid 1px #fc523f;
		text-align: center;
		line-height: 42rpx;
		font-size: 24rpx;
		color: #fc6450;
		margin-top: 15rpx;
	}
	.order-item>.right>view:nth-child(3){
		font-size: 26rpx;
		color: #666666;
		margin-top: 18rpx;
	}
	.order-item>.right>view:nth-child(4){
		font-size: 26rpx;
		color: #666666;
		margin-top: 8rpx;
	}
</style>
