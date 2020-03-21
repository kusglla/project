<template>
	<view class="page">
		<!-- 搜索框 -->
		<view style="height: 200rpx;background: #E9AE43;border-radius: 0rpx 0rpx 20rpx 20rpx;">
			<view style="display: flex;align-items: center;justify-content: space-between; margin: 0rpx 20rpx;padding: 20rpx 0rpx;">
				<view style="font-size: 28rpx;color: #333333;display: flex;justify-content: center;align-items: flex-end;height: 60rpx;">
					<view><image src="../../static/location.png" mode="" style="width: 44rpx;height: 38rpx;"></image></view>
					<view style="line-height: 60rpx;">广州市</view>
					<view><image src="../../static/pull.png" mode="" style="width: 36rpx;height: 40rpx;"></image></view>
				</view>
				<view style="position: relative;height: 60rpx;"> 
					<input style="padding-left: 50rpx;width: 440rpx;font-size: 28rpx;color: #999999;background: #FFFFFF;height: 55rpx;background-color: #ffffff;border-radius: 28px;" class="uni-input" confirm-type="search" placeholder="搜索商家,商品" />
					<image src="../../static/search.png" mode="" style="height: 30rpx;width: 30rpx;position: absolute;top: 14rpx;left: 16rpx;"></image>
				</view>
				<view style="height: 60rpx;display: flex;justify-content: center;align-items: center;" @click="openScanCode()">
					<image src="../../static/saoma.png" mode="" style="width: 38rpx;height: 38rpx;"></image>
				</view>
			</view>
		</view>
		
		<!-- 轮播图 -->
	    <view class="uni-padding-wrap" style="margin-top: -90rpx;height: 277rpx;">
	        <view class="page-section swiper">
	            <view class="page-section-spacing">
	                <swiper class="swiper" :indicator-dots="true" :autoplay="autoplay" :interval="interval" :duration="duration" indicator-color="rgba(225,225,225,1)" indicator-active-color="rgba(225,255,255,.5)">
	                    <swiper-item v-for="item in 4">
	                        <view class="swiper-item">
								<image src="../../static/test.jpg" mode="" style="border-radius: 10rpx;height: 100%;width: 100%;"></image>
							</view>
	                    </swiper-item>
	                </swiper>
	            </view>
	        </view>
	    </view>
		
		<!-- 公告 -->
		<view class="notice-wrap">
			<view>
				<image src="../../static/home/baihuo.png" mode="" style="height: 36rpx;width: 32rpx; padding: 5rpx 10rpx 0rpx;"></image>
				<text style="font-size: 28rpx;">热烈庆祝雍达云商上线啦~~</text>
			</view>
			<view>
				<text style="font-size: 24rpx;color: #999999;" @click="onNotice()">更多 ></text>
			</view>
		</view>
		
		<!-- 导航栏 -->
		<view class="nav-wrap">
			<view v-for="(item,index) in nav" :key='index' @click="onNav(index)">
				<view class="nav-item">
					<image :src="item.img" mode="" style=""></image>
				</view>
				<view><text style="font-size: 26rpx;">{{item.text}}</text></view>
			</view>
		</view>
		
		<!-- 质惠上新 -->
		<view class="newproducts-wrap">
			<view style="position: relative; display: flex;justify-content: space-between;">
				<view>
					<image src="../../static/形状%201@2x.png" mode="" style="height: 76rpx;width: 415rpx;"></image>
					<view style="position: absolute; top: 16rpx;left: 20rpx; display: flex;">
						<view style="font-size: 30rpx;color: #FFFFFF;">质惠商城</view>
						<view style="font-size: 22rpx;color: #333333;margin-left: 24rpx;display: flex;align-items: center;">新品大放送</view>
					</view>
				</view>
				<view style="font-size: 24rpx;display: flex;align-items: flex-end;color: #999999;line-height: 76rpx;">
					好物限时抢 >
				</view>
			</view>
			<view style="display: flex;justify-content: space-around;padding:32rpx 0rpx;">
				<view v-for="item in 4">
					<view style="height: 159rpx;width: 155rpx;background: url(../../static/矩形%201.png);padding: 12rpx 12rpx 16rpx;box-sizing: border-box;">
						<image src="../../static/test.jpg" mode="" style="height: 137rpx;width: 130rpx;"></image>
					</view>
					<view style="font-size: 28rpx;color: #FF3512;text-align: center;margin-top: 17rpx;">￥3399.0</view>
				</view>
			</view>
		</view>
		
		<!-- 秒杀模块 -->
		<view class="full pt-25 pb-25" style="background: #FFFFFF;margin-top: 16rpx;">
			<view style="width: 709rpx;margin: auto; display: flex;justify-content: space-between;">
				<view style="background: #009688;height: 340rpx;width: 327rpx;border-radius: 10rpx;">
					<image src="../../static/test.jpg" mode="" style="height: 100%;width: 100%;border-radius: 10rpx;"></image>
				</view>
				
				<view style="display: flex;flex-direction: column;justify-content: space-between;">
					<view style="background: #009688; height: 155rpx; width: 348rpx; border-radius: 10rpx;"><image src="../../static/test.jpg" mode="" style="height: 100%;width: 100%;border-radius: 10rpx;"></image></view>
					<view style="background: #009688; height: 155rpx; width: 348rpx; border-radius: 10rpx;"><image src="../../static/test.jpg" mode="" style="height: 100%;width: 100%;border-radius: 10rpx;"></image></view>
				</view>
			</view>
		</view>
		
		<!-- 购物分类 -->
		<view class="buytype-wrap">
			<view v-for="(item,index) in nav2" :key="index" @click="onStore(index)" class="buy-item" style="display: flex;flex-direction: column;justify-content: center;align-items: center;">
				<view :class="[index==2? 'img-bg3':'',index==7? 'img-bg7':'']">
					<image :src="item.img" mode=""></image>
				</view>
				
				<view style="font-size: 24rpx;color: #333333;margin-top: 10rpx;">{{item.text}}</view>
			</view>
		</view>
		
		<!-- 五星好评 -->
		<view class="full pt-24" style="background: #E9AE43;">
			<view style="width: 709rpx;margin: 20rpx auto 0rpx; background: #FFFFFF;padding:65rpx 24rpx 100rpx; box-sizing: border-box;;border-radius: 10rpx;">
				<view style="height: 60rpx;text-align: center;width: 350rpx; margin: auto; border-top: 1px solid #999999">
					<view style="width: 200rpx; margin: -26rpx auto 0rpx; background: #FFFFFF;"> 五 星 好 评 </view>
				</view>
				<view style="display: flex; flex-wrap: wrap; justify-content: space-between">
					<view v-for="item in 4" class="goodproduct-item">
						<view>
							<image src="../../static/test.jpg" mode="" style="height: 100%;width: 100%;border-radius: 10rpx;"></image>
						</view>
						<view>黄焖鸡米饭</view>
						<view>￥25</view>
						<view>⭐⭐⭐⭐⭐</view>
					</view>
				</view>
			</view>
		</view>
		
		<!-- 签到 -->
		<view class="sign-day" @click="onSign()">
			签到
		</view>
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello',
				nav:[
					{text:'质惠商城',img:'../../static/home/nav1.png'},
					{text:'特惠专区',img:'../../static/home/nav2.png'},
					{text:'云商嗨购',img:'../../static/home/nav3.png'},
					{text:'厂商直供',img:'../../static/home/nav4.png'},
					{text:'分享赚呗',img:'../../static/home/nav5.png'},
				],
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
		onLoad() {
			
		},
		methods: {
			onNotice(){
				uni.navigateTo({
					url:'../notice/notice'
				})
			},
			
			onNav(e){
				uni.navigateTo({
					url:`../nav/nav${e+1}`
				})
			},
			
			onStore(e){
				uni.navigateTo({
					url:`../partition/partition${e+1}`
				})
			},
			
			openScanCode(){
				uni.scanCode({
				    success: function (res) {
				        console.log('条码类型：' + res.scanType);
				        console.log('条码内容：' + res.result);
				    }
				});
			},
			onSign(){
				uni.navigateTo({
					url:"../sign/sign"
				})
			}
		}
	}
</script>

<style>
	.swiper-item{
		background-color: #4CD964;
		height: 277rpx;
		width: 709rpx;
		margin: auto;
		border-radius: 20rpx!important;
	}
	
	swiper{
		height: 277rpx;
	}
	
	/* 公告栏 */
	.notice-wrap{
		height: 80rpx;
		width: 709rpx;
		margin: auto;
		padding: 25rpx 0rpx;
		box-sizing: border-box;
		display: flex;
		justify-content: space-between;
	}
	
	/* 导航栏 */
	.nav-wrap{
		height: 190rpx;
		padding: 21rpx;
		width: 709rpx;
		margin: auto;
		box-sizing: border-box;
		display: flex;
		justify-content: space-between;
	}
	
	.nav-item{
		width:102rpx;
		height:102rpx;
		border-radius:50%;
		display: flex;
		align-items: center;
		justify-content: center;
	}
	
	.nav-wrap>view:nth-child(1)>.nav-item{
		background:linear-gradient(-18deg,rgba(225,180,95,1),rgba(251,207,150,1));
	}
	
	.nav-wrap>view:nth-child(2)>.nav-item{
		background:linear-gradient(-45deg,rgba(252,107,87,1),rgba(251,56,37,1));
	}
	
	.nav-wrap>view:nth-child(3)>.nav-item{
		background:linear-gradient(-45deg,rgba(241,85,133,1),rgba(250,146,183,1));
	}
	
	.nav-wrap>view:nth-child(4)>.nav-item{
		background:linear-gradient(-45deg,rgba(112,168,254,1),rgba(72,127,254,1));
	}
	
	.nav-wrap>view:nth-child(5)>.nav-item{
		background:linear-gradient(-45deg,rgba(17,168,101,1),rgba(124,236,118,1));
	}
	
	.nav-item image{
		height: 46rpx;
		width: 46rpx;
	}
	
	/* 购物分类 */
	.buytype-wrap{
		width: 709rpx;
		margin: 16rpx auto 0rpx;
		padding: 30rpx 0rpx;
		border-radius: 10rpx;
		background:rgba(255,255,255,1);
		box-shadow:0px 4px 9px 0px rgba(0, 0, 0, 0.07);
		display: flex;
		justify-content: space-between;
		flex-wrap: wrap;
	}
	
	.buytype-wrap image{
		width: 57rpx;
		height: 56rpx;
		margin-top: 10rpx
	}
	
	.buy-item{
		width: 125rpx;
		text-align: center;
		margin-top: 30rpx;
	}
	
	.img-bg3{
		height: 72rpx;
		width: 72rpx;
		border-radius: 50%;
		background: #FF7F3B;
		text-align: center;
	}
	
	.img-bg3>image{
		height: 39rpx;
		width: 32rpx;
		margin-top: 20rpx;
	}
	
	.img-bg7{
		width: 66rpx;
		height: 79rpx;
		text-align: center;
		background: url(../../static/home/tybg.png)no-repeat;
		background-size: 100% 100%;
	}
	.img-bg7>image{
		height: 38rpx;
		width: 35rpx;
		margin-top: 15rpx;
	}
	
	
	/* 新品 */
	.newproducts-wrap{
		width: 709rpx;
		margin: auto;background:rgba(255,255,255,1);
		box-shadow:0px 4px 9px 0px rgba(0, 0, 0, 0.07);
		border-radius:8px;
	}
	
	
	/* 五星好评 */
	.goodproduct-item{
		margin-top: 20rpx;
	}
	
	.goodproduct-item>view:nth-child(1){
		width: 310rpx;
		height: 232rpx;
	}
	.goodproduct-item>view:nth-child(2){
		font-size:28rpx;
		font-weight:700;
		color:rgba(51,51,51,1);
	}
	.goodproduct-item>view:nth-child(3){
		font-size:32rpx;
		font-weight:bold;
		color:rgba(249,47,59,1);
	}
	.goodproduct-item>view:nth-child(4){
		
	}
	
	
	/* 签到 */
	.sign-day{
		width:152rpx;
		height:62rpx;
		background:rgba(251,65,46,1);
		border-radius: 31rpx 0rpx 0rpx 31rpx;
		color: #FFFFFF;
		position: fixed;
		right: 0rpx;
		bottom: 200rpx;
		text-align: center;
		line-height: 62rpx;
	}
	
</style>
