<template>
	<view class="page">
		<view class="share-item" v-for="item in 4">
			<view class="item-top">
				<view class="left"><image src="../../static/test.jpg" mode="" style="height: 100%;width: 100%;border-radius: 10rpx;"></image></view>
				<view class="right">
					<view>NOISE 音乐家教练夹克</view>
					<view>邀请一好友实名认证可获得20通呗</view>
					<view><text style="color: #ff923c;">已发放569通呗</text><text>/共80000通</text></view>
					<view>
						 <progress percent="40" border-radius="10rpx" activeColor="#fdcd60" backgroundColor="#ff923c" />
					</view>
				</view>
			</view>
			
			<view class="item-bottom">
				<view>分享至</view>
				<view>微信好友</view>
				<view>朋友圈</view>
			</view>
		</view>
		
		<view class="warn">!要推荐新用户注册才能得到同呗</view>
	</view>
</template>

<script>
</script>

<style>
	.share-item{
		margin-top: 20rpx;
		padding: 0rpx 35rpx;
		border-bottom: 1px solid #CCCCCC;
	}
	
	.item-top{
		display: flex;
		border-bottom: 1rpx dashed #EEEEEE;
		padding-bottom: 26rpx;
	}
	
	.item-top>.left{
		width: 184rpx;
		height: 191rpx;
		border-radius: 10rpx;
	}
	
	.item-top>.right{
		margin-left: 23rpx;
	}
	
	.item-top>.right>view:nth-child(1){
		font-size: 30rpx;
		color: #333333;
	}
	.item-top>.right>view:nth-child(2){
		font-family: PingFang-SC-Medium;
		font-size: 26rpx;
		font-weight: normal;
		font-stretch: normal;
		letter-spacing: 2rpx;
		color: #666666;
		margin-top: 19rpx;
	}
	.item-top>.right>view:nth-child(3){
		font-family: PingFang-SC-Medium;
		font-size: 26rpx;
		letter-spacing: 2rpx;
		color: #666666;
		margin-top: 36rpx;
	}
	.item-top>.right>view:nth-child(4){
		margin-top: 15rpx;
	}
	
	.item-bottom{
		font-size: 26rpx;
		display: flex;
		padding: 25rpx 0rpx;
	}
	
	.item-bottom>view:nth-child(1){
		font-size: 26rpx;
		letter-spacing: 2px;
		color: #666666;
	}
	.item-bottom>view:nth-child(2){
		margin-left: 253rpx;
	}
	.item-bottom>view:nth-child(3){
		margin-left: 60rpx;
	}
	
	.warn{
		font-size: 24rpx;
		color: #666666;
		margin-top: 266rpx;
		margin-bottom: 40rpx;
		text-align: center;
	}
</style>
