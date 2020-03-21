<template>
	<view class="page">
		<view style="width: 420rpx;height: 297rpx;margin: 184rpx auto 0rpx;display: flex;flex-direction: column;align-items: center;justify-content: space-between;">
			<view>
				<image src="../../static/test.jpg" mode="" style="width: 153rpx;height: 153rpx; border-radius: 50%;"></image>
			</view>
			<view style="font-size: 32rpx;">需要实名认证才可以开启推广</view>
			<view style="font-size: 32rpx;color: #e4ac43;" @click="onRealname">前往实名></view>
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
			onRealname(){
				uni.navigateTo({
					url:'../realname/realname'
				})
			}
		}
	}
</script>

<style>

</style>
