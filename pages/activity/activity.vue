<template>
	<view class="page">
		<!-- 类型切换 -->
		<view style="height: 182rpx;padding-top: 60rpx;box-sizing: border-box; background: url(../../static/top-bg.png) no-repeat;background-size: 100% 100%;">
			
			<view style="display: flex;">
				<view style="width: 50%; text-align: center;" @click="tabType(0)">
				    <text  style="padding-bottom: 19rpx;" :class="[type==0? 'active-line':'']">云商秒嗨</text>
				</view>
				<view style="width: 50%; text-align: center;" @click="tabType(1)">
				    <text style="padding-bottom: 19rpx;" :class="[type==1? 'active-line':'']">嗨翻同城</text>
				</view>
			</view>
		</view>
		
		<!-- 秒杀time -->
		<view class="miaosha-time">
			<view @click="selectTime(0)">
				<view :class="[timetype==0? 'active-time':'']">15:00</view>
				<view :class="[timetype==0? 'active-bg':'']">秒杀中</view>
			</view>
			
			<view @click="selectTime(1)">
				<view :class="[timetype==1? 'active-time':'']">20:00</view>
				<view :class="[timetype==1? 'active-bg':'']">即将开始</view>
			</view>
			
			<view @click="selectTime(2)">	
				<view :class="[timetype==2? 'active-time':'']">24:00</view>
				<view :class="[timetype==2? 'active-bg':'']">即将开始</view>
			</view>
		</view>
		
		<!-- order -->
		<view class="pl-25 pr-25">
			<view class="order-wrap">
				<view v-for="item in 3" class="order-item">
					
					<view class="left">
						<image src="../../static/test.jpg" mode="" style="width: 172rpx;height: 172rpx;border-radius: 10rpx;"></image>
					</view>
					
					<view class="right">
						<view>嘻游记原创 悠闲两面穿外套 宽松显瘦大衣女中长秋冬新款</view>
						<view>
							<text style="font-size:32rpx;">￥500 + 56</text> 
							<text style="font-size:24rpx;color: #FB4632;">同呗</text>
							<text style="font-size26rpx;color:#999999; text-decoration: inherit;">￥5000.00</text>
						</view>
					</view>
				</view>
			</view>
		</view>
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				type:0,
				timetype:0
			}
		},
		methods: {
			tabType(e){
				this.type=e
				console.log(e)
			},
			selectTime(e){
				this.timetype = e
			}
		}
	}
</script>

<style>
	/* 秒杀时间 */
	.active-time{
		font-size: 32rpx!important;
		color: #FB4431!important;
	}
	
	.active-bg{
		background:rgba(251,67,48,1);
		height: 46rpx;
		border-radius:23px;
		color: #FFFFFF!important;
		font-size: 32rpx;
	}
	
	.active-line{
		border-bottom: 5px solid #FB4330;
		color: #FB4330;
	}
	
	.miaosha-time{
		display: flex;
		justify-content: space-between;
		padding: 20rpx 50rpx;
	}
	
	.miaosha-time>view{
		width: 160rpx;
		text-align: center;
	}
	
	.miaosha-time>view>view:nth-child(1){
		color: #333333;
	}
	
	.miaosha-time>view>view:nth-child(2){
		font-size: 28rpx;
		color: #999999;
		line-height: 46rpx;
	}
	
	
	/* 秒杀order */
	.order-wrap{
		box-sizing: border-box;
		border-radius: 10rpx;
		padding: 30rpx;
		background:rgba(255,255,255,1);
		box-shadow:0px 4px 9px 0px rgba(0, 0, 0, 0.07);
	}
	
	.order-item{
		 display: flex;
		 justify-content: space-between;
		 margin-top: 33rpx;
	}
	
	.order-item>.left{
	}
	
	.order-item>.right{
		 width: 435rpx;
		 display: flex;
		 flex-direction: column;
		 justify-content: space-between;
	}
	
	.order-item>.right{
		 font-size:28rpx;
		 font-weight:700;
		 color:rgba(51,51,51,1);
	}
	
	
</style>
