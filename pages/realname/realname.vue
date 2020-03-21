<template>
	<view class="page">
		<view style="height: 20rpx;background: #f7f7f7;"></view>
		
		<view class="realname-page">
			<view> <text>姓名</text> <input type="text" placeholder="请输入姓名" v-model="name" /></view>
			<view> <text>身份证号码</text> <input type="text" placeholder="请输入身份证号码" v-model="idCard" /></view>
			<view> <text>手机号</text> <input type="text" placeholder="请输入手机号" v-model="phone" /></view>
			<view> <text>验证码</text> <input type="text" placeholder="请输入验证码" v-model="phoneCode" /></view>
		</view>
		
		<view style="margin-top: 184rpx;"><button type="default" class="btn">申请</button></view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				name:'',
				idCard:'',
				phone:'',
				phoneCode:''
			}
		},
		methods: {
			
		}
	}
</script>

<style>
	.realname-page{
		padding: 0rpx 20rpx;
	}
	
	.realname-page view{
		display: flex;
		border-bottom: 1rpx solid #eeeeee;
		padding: 30rpx 0rpx;
	}
	
	.realname-page view text{
		width: 250rpx;
		color: #333333;
	}
	
	.btn{
		width: 386rpx;
		height: 80rpx;
		background-image: linear-gradient(#f3be5b,#f3be5b), 
		linear-gradient(90deg, 
			#1228f6 0%, 
			#337bff 60%, 
			#33b0ff 100%);
		background-blend-mode: normal, 
			normal;
		border-radius: 40px;
		font-size: 34rpx;
		color: #ffffff;
	}
</style>
