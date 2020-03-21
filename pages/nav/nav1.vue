<template>
	<view>
		<view class="msg">
			<view style="padding: 0rpx 10rpx;"><image src="../../static/home/baihuo.png" mode="" style="width: 32rpx;height: 36rpx;"></view></image>
			<text style="font-size: 24rpx;color: #666666;">任意购买一款质惠商城的商品就可以获得好友佣金喔~</text>
		</view>
		
		<view style="height: 10rpx;background: #EEEEEE;"></view>
		
		<!-- 分类 -->
		<view class="buytype-wrap">
			<view v-for="(item,index) in nav2" :key="index" @click="onStore(index)" class="buy-item" style="display: flex;flex-direction: column;justify-content: center;align-items: center;">
				<view :class="[index==2? 'img-bg3':'',index==7? 'img-bg7':'']">
					<image :src="item.img" mode=""></image>
				</view>
				
				<view style="font-size: 24rpx;color: #333333;margin-top: 10rpx;">{{item.text}}</view>
			</view>
		</view>
		
		<!-- 搜索栏 -->
		<view class="search-box" style="padding: 20rpx; box-sizing: border-box;position: relative;">
			<image src="../../static/search.png" mode="" style="position: absolute;height: 30rpx;width: 30rpx;left: 40rpx;top: 40rpx;"></image>
			 <input style="height: 66rpx; background-color: #ffffff;border-radius: 30rpx; font-size: 26rpx; padding-left: 50rpx;" class="uni-input" confirm-type="search" placeholder="请输入商品名称" />
		</view>
		
		<!-- 商品 -->
		<view class="order-list">
			<view v-for="(item,index) in 4" :key="index" @click="onDetail()" class="order-item">
				<view><image src="../../static/test.jpg" mode="" style="height: 223rpx;width: 308rpx;border-radius: 10rpx;"></image></view>
				<view class="product-text">嬉游记原创 休闲两面穿外套 宽松显瘦大衣女款</view>
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
			onDetail(){
				uni.navigateTo({
					url:'../detail/detail'
				})
			}
		}
	}
</script>

<style>
	.msg{
		height: 82rpx;
		background-color: #FFFFFF;
		color: #F7F7F7;
		padding: 0rpx 30rpx;
		display: flex;
		justify-content: center;
		align-items: center;
	}
	
	.buytype-wrap{
		width: 709rpx;
		margin: 16rpx auto 0rpx;
		padding: 30rpx 0rpx;
		border-radius: 10rpx;
		display: flex;
		justify-content: space-between;
		flex-wrap: wrap;
	}
	
	/* 购物分类 */
	.buytype-wrap{
		width: 709rpx;
		margin: 16rpx auto 0rpx;
		padding: 30rpx 0rpx;
		border-radius: 10rpx;
		background:rgba(255,255,255,1);
		box-shadow:0px 4px 9px 0px rgba(0, 0, 0, 0.07);
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
	
	
	/* 搜索栏 */
	.search-box{
		width:750rpx;
		height:101rpx;
		background:rgba(225,180,95,1);
	}
	
	/* order */
	.order-list{
		display: flex;
		justify-content: space-between;
		flex-wrap: wrap;
		padding: 30rpx 40rpx;
		box-sizing: border-box;
	}
	
	.order-item{
		width: 308rpx;
		margin-top: 40rpx;
	}
	
	.order-item>view:nth-child(1){
		width: 308rpx;
		height: 223rpx;
		border-radius: 10rpx;
	}
	
	.order-item>view:nth-child(2){
		width: 305rpx;
		overflow: hidden;
		text-overflow: ellipsis;
		font-size:28rpx;
		font-weight:500;
		color:rgba(51,51,51,1);
		margin-top: 23rpx;
	}
	
	.order-item>view:nth-child(3){
		font-size:32rpx;
		font-weight:500;
		color:rgba(251,70,50,1);
		margin-top: 23rpx;
	}
	
	.order-item>view:nth-child(4){
		font-size:24rpx;
		font-weight:500;
		color:rgba(153,153,153,1);
		margin-top: 7rpx;
	}
</style>
