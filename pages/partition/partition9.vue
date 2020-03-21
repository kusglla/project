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
		
		<!-- 附近门店 -->
		<view class="nearby-wrap">
			<view>附近门店</view>
			<view>朝阳区建国门外大姐</view>
		</view>
		
		<view class="order-wrap">
			<view class="product-item" v-for="item in 4">
				<view class="left"><image src="../../static/test.jpg" mode="" style="height: 100%;width: 100%;border-radius: 10rpx;"></image></view>
				<view class="right">
					<view>兴盛世家城北店</view>
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
		data(){
			return{
				nav2:[
					{text:'超市百货',img:'../../static/home/lanzi.png'},
					{text:'蔬菜水果',img:'../../static/home/shuiguo.png'},
					{text:'小吃门店',img:'../../static/home/meishi.png'},
					{text:'日用百货',img:'../../static/home/baihuo.png'},
					{text:'服饰专区',img:'../../static/home/qunzi.png'},
					{text:'休闲零食',img:'../../static/home/lingshi.png'},
					{text:'甜点饮品',img:'../../static/home/tiandian.png'},
					{text:'酒店',img:'../../static/home/jiudian.png'},
					{text:'便民专区',img:'../../static/home/bianmin.png'},
					{text:'更多',img:'../../static/home/gengduo.png'},
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
		padding: 0rpx 20rpx;
		margin: auto;
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
	
	/* 附近门店 */
	.nearby-wrap{
		padding: 0rpx 20rpx;
		margin-top: 80rpx;
		display: flex;
	}
	
	.nearby-wrap>view:nth-child(1){
		font-size: 32rpx;
		color: #333333;
	}
	
	.nearby-wrap>view:nth-child(2){
		margin-left: 69rpx;
		font-size: 24rpx;
		color: #999999;
		display: flex;
		flex-direction: column;
		justify-content: flex-end;
	}
	
	/* 商品列表 */
	.order-wrap{
		padding: 0rpx 20rpx;
		margin-top: 30rpx;
	}
	.product-item{
		display: flex;
		margin-top: 25rpx;
	}
	.product-item>.left{
		height: 195rpx;
		width: 243rpx;
		border-radius: 10rpx;
	}
	.product-item>.right{
		margin-left: 36rpx;
	}
	.product-item>.right>view:nth-child(1){
		font-size: 28rpx;
		letter-spacing: 2px;
		color: #333333;
	}
	.product-item>.right>view:nth-child(2){
		width: 85rpx;
		height: 42rpx;
		border-radius: 10rpx;
		border: solid 1px #fc523f;
		font-size: 24rpx;
		color: #fc6450;
		line-height: 42rpx;
		text-align: center;
		margin-top: 15rpx;
	}
	.product-item>.right>view:nth-child(3){
		font-size: 26rpx;
		color: #666666;
		margin-top: 22rpx;
	}
	.product-item>.right>view:nth-child(4){
		font-family: PingFang-SC-Medium;
		font-size: 26rpx;
		letter-spacing: 2rpx;
		color: #666666;
		margin-top: 8rpx;
	}
</style>
