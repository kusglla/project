<template>
	<view class="page">
		<view class="top-bg">
			<view @click="onMyInfo()">个人信息></view>
		</view>
		
		<view class="message-wrap">
			<view class="message-content">
				<view><image src="../../static/test.jpg" style="width: 200rpx;height: 200rpx;border-radius: 50%; margin-top: -100rpx;" mode=""></image></view>
				<view>无印良品</view>
				<view>广东省广州市天河区天河大道151号</view>
			</view>
		</view>
		
		
		<view class="admin-wrap">
			<view @click="onMoneyAdmin()">
				<view><image src="../../static/home/bianmin.png" style="width: 95rpx;height: 97rpx;" mode=""></image></view>
				<view>财务管理</view>
			</view>
			<view @click="onStoreAdmin()">
				<view><image src="../../static/home/bianmin.png" style="width: 95rpx;height: 97rpx;" mode=""></image></view>
				<view>商家管理</view>
			</view>
			<view @click="onPassAdmin()">
				<view><image src="../../static/home/bianmin.png" style="width: 95rpx;height: 97rpx;" mode=""></image></view>
				<view>审核管理</view>
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
		methods:{
			onMyInfo(){
				uni.navigateTo({
					url:"./myinfo"
				})
			},
			onMoneyAdmin(){
				uni.navigateTo({
					url:"./moneyadmin"
				})
			},
			onStoreAdmin(){
				uni.navigateTo({
					url:"./storeadmin"
				})
			},
			onPassAdmin(){
				uni.navigateTo({
					url:"./passadmin"
				})
			},
		}
	}
</script>

<style>
	.top-bg{
		width:750rpx;
		height:215rpx;
		display: flex;
		justify-content: flex-end;
		color: #FFFFFF;
		font-size: 24rpx;
		padding: 30rpx;
		box-sizing: border-box;
	}
	
	.message-wrap{
		height: 350rpx;
		width: 100%;
		background: #FFFFFF;
	}
	
	.message-content{
		text-align: center;
	}
	
	.message-content>view:nth-child(1){
	}
	
	.message-content>view:nth-child(2){
		font-size: 32rpx;
		color: #333333;
		margin-top: 10rpx;
	}
	
	.message-content>view:nth-child(3){
		font-size: 26rpx;
		color: #999999;
		margin-top: 20rpx;
	}
	
	.admin-wrap{
		margin: -90rpx 45rpx;
		padding: 30rpx 50rpx;
		box-sizing: border-box;
		display: flex;
		justify-content: space-between;
		/* height:227px; */
		background:rgba(255,255,255,1);
		box-shadow:0px 0px 18px 2px rgba(0, 0, 0, 0.24);
	}
	
	.admin-wrap>view>view{
		text-align: center;
	}
	
	.admin-wrap>view>view:nth-child(2){
		margin-top: 25rpx;
		font-size: 26rpx;
		color: #333333;
	}
</style>
