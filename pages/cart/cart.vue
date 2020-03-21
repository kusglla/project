<template>
	<view class="page">
		<view class="top-bg">
			
		</view>
		
		<view style="margin-top: -120rpx;">
			<view class="cart-block-item" v-for="(item,index) in cartItem" :key="index">
				<view style="margin: auto;">
					<label class="radio">
						<radio value="" /><text></text>
					</label>
				</view>
				<view class="cart-cover"><image src="../../static/test.jpg" mode="" style="width: 184rpx;height: 184rpx;border-radius: 5rpx;"></image></view>
				<view style="display: flex;flex-direction: column;justify-items: space-between;">
					<view class="product-title">嘻游记原创 休闲两面外套</view>
					<view class="size">均码</view>
					<view class="prict-number">
						<view class="prict">$329.00</view>
						<view></view>
					</view>
				</view>
			</view>
		</view>
		
		<!-- 底部结算 -->
		<view style="color: #999999;margin: 0rpx 20rpx;box-sizing: border-box; font-size: 28rpx;height: 100rpx;width: 100%;border-top:1rpx solid #dddddd; position: fixed;bottom: 0;left: 0; display: flex;justify-items: space-between;align-items: center;">
			<view>
				<label class="radio">
					<radio value=""  style="width: 28rpx;height: 28rpx;transform: scale(0.7)"/>
					<text style="margin-left: 20rpx;">全选 删除</text>
				</label>
			</view>
			<view style="margin-left: 60rpx;">合计:<text style="color: #f94d43;;">￥25+5625通呗</text></view>
			<button class="mini-btn" type="default" size="mini" style="width: 160rpx;height: 66rpx;border-radius: 33rpx;color: #FFFFFF;font-size: 32rpx;line-height: 66rpx;background: #e64b1d;">结算</button>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				cartItem:2
			}
		},
		methods: {
			
		}
	}
</script>

<style>
	.cart-block-item{
		width: 712rpx;
		height: 252rpx;
		margin: auto;
		padding: 34rpx 25rpx;
		margin-top: 21rpx;
		background-color: #ffffff;
		box-shadow: 0px 2px 20px 0px
		rgba(0, 0, 0, 0.02);
		box-sizing: border-box;
		border-radius: 20px;
		display: flex;
	}
	.cart-cover{
		padding: 0rpx 25rpx;
	}
	
	.product-title{
		width: 373rpx;
		height: 52rpx;
		font-size: 24rpx;
		letter-spacing: 1px;
		color: #333333;
	}
	
	.size{
		width: 48px;
		height: 22px;
		font-size: 23rpx;
		line-height: 24px;
		letter-spacing: 1px;
		color: #999999;
	}
	
	.prict{
		color: #e94b22;
	}
	
	.prict-number{
		display: flex;
		justify-items: space-between;
	}
	
	.bottom-box{
		position: absolute;
		bottom: 0;
		left: 0;
		border-bottom: 1rpx solid #999;
	}
	
</style>
