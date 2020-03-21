<template>
	<view class="page">
		<!-- 轮播 -->
		<view style="height: 428rpx;">
			<image src="../../static/test.jpg" mode="" style="width: 100%;height: 100%;"></image>
		</view>
		
		
		<view style="padding: 0rpx 30rpx;">
			<view style="margin-top: 30rpx;">Ayuko 时髦气质毛呢外套 加棉可脱卸呢大衣</view>
			
			<view style="display: flex;justify-content: space-between; margin-top: 30rpx;">
				<view><text style="font-size: 38rpx;color: #f92f3b;">￥5000.00</text><text style="color: #aaaaaa;text-decoration: dashed;">￥8000.00</text></view>
				<view style="font-size: 24rpx;color: #999999;display: flex;align-items: flex-end;">剩余56件</view>
			</view>
			
			<view style="display: flex;justify-content: space-between;margin-top: 60rpx;">
				<view class="bg">+5000积分</view>
				<view style="display: flex;">
					<view class="bg" style="margin-right: 20rpx;">+5000同呗</view>
					<view class="bg">+5000消费</view>
				</view>
			</view>
			
			<view style="font-size: 30rpx;color: #666666;display: flex;justify-content: space-between;margin-top: 60rpx;" @click="chooseSize()">
				<view>规格选择</view>
				<view>></view>
			</view>
			
			<view class="" style="display: flex;justify-content: space-around;margin-top: 60rpx;">
				<view style="padding: 13rpx 16rpx;" @click="tabType(0)" :class="[type==0? 'active':'']">详情</view>
				<view style="padding: 13rpx 16rpx;" @click="tabType(1)" :class="[type==1? 'active':'']">评价(526)</view>
			</view>
		</view>
		<!-- 加入 -->
		<view class="add-wrap">
			<view class="left">
				<view class="">
					<image src="../../static/home/bianmin.png" style="height: 40rpx;width: 40rpx;" mode=""></image>
					<text>首页</text>
				</view>
				<view class="">
					<image src="../../static/home/baihuo.png" style="width: 39rpx;height: 36rpx;" mode=""></image>
					<text>收藏</text>
				</view>
			</view>
			<view class="right">
				<view>加入购物车</view>
				<view>立即购买</view>
			</view>
		</view>
		
		
		<!-- 评价 -->
		<view class="pingjia-wrap" v-if="type==1">
			
			<view class="chooserink-wrap">
				<view class="pingjia-bg" :class="[scoretype==0?'select-pingjia-bg':'']" @click="checkGrade(0)">全部</view>
				<view class="pingjia-bg" :class="[scoretype==1?'select-pingjia-bg':'']" @click="checkGrade(1)">好评</view>
				<view class="pingjia-bg" :class="[scoretype==2?'select-pingjia-bg':'']" @click="checkGrade(2)">中评</view>
				<view class="pingjia-bg" :class="[scoretype==3?'select-pingjia-bg':'']" @click="checkGrade(3)">差评</view>
			</view>
			
			<view class="pinglun-item" v-for="item in 4">
				<view><image src="../../static/test.jpg" mode="" style="width: 100%;height: 100%;border-radius: 50%;"></image></view>
				
				<view>
					<view style="font-size: 32rpx;">姓名</view>
					<view style="font-size: 26rpx;">2019-05-05 14:55:20 红色</view>
					<view style="font-size: 26rpx;">评价内容,非常不错,赞~~</view>
					<view></view>
				</view>
				
				<view style="width: 87rpx;height: 43rpx;line-height: 43rpx; font-size:23rpx;text-align: center; ;border-radius: 10rpx;border: solid 1px #ff923c;">好评</view>
			</view>
		</view>
		
		
		
		
		<!-- 弹出层 -->
		<uni-popup ref="popup" type="bottom">
			<view class="popup-wrap">
				<view class="info-wrap">
					<view><image src="../../static/test.jpg" mode="" style="width: 100%;height: 100%;"></image></view>
					<view>
						<view>Ayuko 时髦气质毛呢外套 加棉可脱卸呢大衣</view>
						<view style="color: #f92f3b;">
							<text>￥5000.00</text>
							<text>库存56件</text>
						</view>
					</view>
				</view>
				
				<view class="color-wrap">
					<view>颜色</view>
					<view>
						<view class="size-bg" v-for="item in 3">白色</view>
					</view>
				</view>
				<view class="size-wrap">
					<view>数量</view>
					<view>-2+</view>
				</view>
				<view style=""> <button type="primary" style="margin-top: 30rpx;" @click="onBuy()">确定</button> </view>
			</view>
		</uni-popup>
	</view>
</template>

<script>
	import uniPopup from '../../components/uni-popup/uni-popup.vue'
	export default {
		data() {
			return {
				type:0,
				scoretype:0
			}
		},
		methods: {
			tabType(e){
				console.log(e)
				this.type = e
			},
			
			// 选择规格
			chooseSize(){
				this.$refs.popup.open()
			},
			
			// 查看评价
			checkGrade(e){
				this.scoretype=e
			},
			
			// 去购买
			onBuy(){
				uni.navigateTo({
					url:'../account/account'
				})
			}
		},
		components:{
			uniPopup
		}
	}
</script>

<style>
	/* 评价 */
	.pingjia-wrap{
		margin: 0rpx 20rpx;
		box-sizing: border-box;
	}
	
	.chooserink-wrap{
		display: flex;
		margin-top: 50rpx;
	}
	
	
	.pingjia-bg{
		width: 130rpx;
		height: 52rpx;
		background-color: #dedbdb;
		color: #999999;;
		border-radius: 26rpx;
		display: flex;
		justify-content: center;
		align-items: center;
		margin-right: 20rpx;
	}
	
	.select-pingjia-bg{
		background-color: #ff923c;
		color: #FFFFFF;
	}
	
	.pinglun-item{
		display: flex;
		margin-top: 25rpx;
		height: 132rpx;
		align-items: center;
	}
	.pinglun-item>view:nth-child(1){
		width: 100rpx;
		height: 100rpx;
		border-radius: 50%;
	}
	.pinglun-item>view:nth-child(2){
		width: 450rpx;
		margin-left: 30rpx;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
	}
	.pinglun-item>view:nth-child(3){
		
	}
	
	.bg{
		width: 130rpx;
		height: 49rpx;
		background-color: #fddcc7;
		color: #fd6707;
		font-size: 22rpx;
		display: flex;
		justify-content: center;
		align-items: center;
	}
	
	.active{
		border-bottom: 8rpx solid #ff923c;
		color: #fd7422;
	}
	
	/* 底部 */
	.add-wrap{
		height: 125rpx;
		width: 100%;
		position: fixed;
		bottom: 0rpx;
		padding: 0rpx 23rpx;
		display: flex;
		padding-top: 10rpx;
		display: flex;
		justify-content: space-between;
		box-sizing: border-box;
		background: #FFFFFF;
	}
	.add-wrap>.left{
		height: 87rpx;
		display: flex;
		font-size: 28rpx;
		color: #333333;
	}
	.add-wrap>.left>view{
		height: 100%;
		width: 70rpx;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		align-items: center;
	}
	.add-wrap>.left>view:nth-child(2){
		margin-left: 40rpx;
	}
	.add-wrap>.right{
		width: 482rpx;
		height: 87rpx;
		border-radius: 0px 44rpx 44rpx 0px;
		display: flex;
		font-family: SourceHanSansCN-Medium;
		font-size: 32rpx;
		color: #ffffff;
		line-height: 87rpx;
		text-align: center;
	}
	.add-wrap>.right>view:nth-child(1){
		width: 50%;
		border-radius: 44rpx 0rpx 0rpx 44rpx;
		background: #323838;;
	}
	.add-wrap>.right>view:nth-child(2){
		width: 50%;
		border-radius: 0rpx 44rpx 44rpx 0rpx;
		background: #f33b3b;
	}
	/* 规格选择 */
	.popup-wrap{
		height: 650rpx;
		background: #FFFFFF;
		border-radius: 20rpx 20rpx 0rpx 0rpx;
		padding: 78rpx 30rpx 30rpx;
	}
	
	.popup-wrap>.info-wrap{
		display: flex;
	}
	
	.popup-wrap>.info-wrap>view:nth-child(1){
		height: 140rpx;
		width: 140rpx;
	}
	.popup-wrap>.info-wrap>view:nth-child(2){
		width: 495rpx;
		margin-left: 37rpx;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		font-size: 38rpx;
	}
	
	
	/* 码数 */
	.size-bg{
		background: #bbbbbb;
		border-radius: 32rpx;
		width: 140rpx;
		height: 63rpx;
		color: #FFFFFF;
		text-align: center;
		line-height: 63rpx;
		margin-top: 20rpx;
		margin-right: 20rpx;
	}
	
	.popup-wrap>.color-wrap{
		font-size: 32rpx;
		color: #333333;
	}
	
	.popup-wrap>.color-wrap>view:nth-child(1){
		color: #333333;
		margin-top: 30rpx;
	}
	.popup-wrap>.color-wrap>view:nth-child(2){
		display: flex;
		margin-top: 30rpx;
	}
	
	.popup-wrap>.size-wrap{
		display: flex;
		justify-content: space-between;
		margin-top: 50rpx;
		padding: 30rpx 0rpx;
		border-top: 1rpx solid #eeeeee;
	}
</style>
