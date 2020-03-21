<template>
	<view class="page">
		<view class="search-box" style="padding: 20rpx; box-sizing: border-box;position: relative;">
			<image src="../../static/search.png" mode="" style="position: absolute;height: 30rpx;width: 30rpx;left: 40rpx;top: 40rpx;"></image>
			 <input style="height: 66rpx; background-color: #ffffff;border-radius: 30rpx; font-size: 26rpx; padding-left: 50rpx;" class="uni-input" confirm-type="search" placeholder="请输入商品名称" />
		</view>
		
		
		<view class="order-wrap">
			<view class="product-item" v-for="item in 4" @click="onDetail()">
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
			onDetail(){
				console.log(2)
				uni.navigateTo({
					url:'../storedetail/storedetail'
				})
			}
		}
	}
</script>

<style>
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
	
	/* 搜索栏 */
	.search-box{
		width:750rpx;
		height:101rpx;
		background:rgba(225,180,95,1);
	}
</style>
