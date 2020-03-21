<template>
	<view class="page">
		<view class="msg-wrap">
			<view class="msg-item">
				<view>姓名</view>
				<view><input type="text" value="" placeholder="小红" disabled/></view>
			</view>
			<view class="msg-item">
				<view>联系方式</view>
				<view><input type="text" value="" placeholder="14163562852" disabled/></view>
			</view>
			<view class="msg-item">
				<view>代理地区</view>
				<view><input type="text" value="" placeholder="广东省广州市白云区" disabled/></view>
			</view>
			<view class="msg-item">
				<view>注册代理时间</view>
				<view><input type="text" value="" placeholder="2020-02-20  20:20:20" disabled/></view>
			</view>
			<view class="msg-item">
				<view>现有商家</view>
				<view><input type="text" value="" placeholder="20" disabled/></view>
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
			
		}
	}
</script>

<style>
	.msg-wrap{
		margin: 0rpx 40rpx;
		box-sizing: border-box;
	}
	
	.msg-item{
		display: flex;
		align-items: center;
		height: 85rpx;
	}
	
	.msg-item>view{
		width: 200rpx;
	}
	
	.msg-item>view:nth-child(1){
		width: 200rpx;
	}
	
	.msg-item>view:nth-child(2){
		margin-left: 40rpx;
	}
	
	input{
		width: 420rpx;
	}
</style>
