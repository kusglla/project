<template>
	<view class="page">
		<view style="height: 750rpx;width: 750rpx;position: absolute;left: 0;top: 0;">
			<image src="../../static/sign-bg.png" mode="" style="width: 100%;height: 100%;"></image>
		</view>
		
		<view class="topbox-wrap">
			<view class="topbox-content">
				<view>连续签到赢通呗</view>
				<view>Sign in consecutively to win tong bai</view>
				<image src="../../static/gift.png" mode="" style="width: 330rpx;height: 321rpx;"></image>
			</view>
		</view>
		
		<view class="signinfo-wrap">
			<view style="display: flex;justify-content: space-around;">
				<view style="text-align: center;">
					<view style="color: #777777;">已连续签到</view>
					<view style="margin-top: 30rpx;">2 <text>天</text></view>
				</view>
				<view style="text-align: center;">
					<view style="color: #777777;">累计签到</view>
					<view style="margin-top: 30rpx;">1232 <text>天</text></view>
				</view>
			</view>
			
			<view style="display: flex;justify-content: space-between;margin-top: 86rpx;color: #8F8F8F;font-size: 22rpx;">
				<view v-for="item in 6" style="text-align: center;">
					<view>待签</view>
					<view><image src="../../static/qian.png" mode="" style="width: 48rpx;height: 48rpx;"></image></view>
					<view>星期{{item+1}}</view>
				</view>
			</view>
			
			<view style="margin:50rpx auto;position: relative;display: flex;justify-content: center;align-items: center;color: #FFFFFF;" @click="signDay()">
				<image src="../../static/yuan.png" mode="" style="width: 210rpx;height: 210rpx;"></image>
				<view style="position: absolute;text-align: center;">
					<view style="font-size:34rpx;">立即签到</view>
					<view style="font-size: 24rpx;">可获得156同呗</view>
				</view>
			</view>
			
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
			signDay(){
				console.log('签到')
			}
		}
	}
</script>

<style>
	.sign-wrap{
		padding:100rpx 30rpx 0rpx;
		position: absolute;
		z-index: 1002;
		top: 430rpx;
		margin: 0rpx 30rpx;
		box-sizing: border-box;
		height:765rpx;
		width: 690rpx;
		background:rgba(255,255,255,1);
		border-radius:15px;
	}
	
	.signinfo-wrap{
		height:765rpx;
		width: 690rpx;
		padding:100rpx 30rpx 0rpx;
		position: absolute;
		z-index: 1002;
		top: 430rpx;
		margin: 0rpx 30rpx;
		box-sizing: border-box;
		background:rgba(255,255,255,1);border-radius:15px;
	}
	
	.page{
		width: 100%;
		height: 100%;
		background: #e9ae43;
	}
	
	.topbox-wrap{
		width: 100%;
		position: absolute;
		z-index: 9999;
		margin-top: 80rpx;
	}
	
	.topbox-content{
		text-align: center;
	}
	
	.topbox-content>view:nth-child(1){
		font-size:76rpx;
		color:rgba(255,255,255,1);
		text-shadow:0px 7px 9px rgba(53,26,122,0.4);
	}
	.topbox-content>view:nth-child(2){
		font-size:30rpx;
		font-weight:normal;
		color:rgba(255,255,255,1);
		text-shadow:0px 7px 9px rgba(53,26,122,0.4);
	}
	.topbox-content>view:nth-child(3){}
</style>
