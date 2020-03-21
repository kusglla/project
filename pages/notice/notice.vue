<template>
	<view class="page" style="margin: 25rpx; box-sizing: border-box;">
		<view style="width: 711rpx; height: 229rpx;">
			<swiper :indicator-dots="true" :autoplay="true" :interval="3000" :duration="1000">
				<swiper-item>
					<view class="swiper-item">
						<h3>《新疆、西藏地区暂停发货》</h3>
						<view>按快递公司通知,西藏、西藏地区的快递暂停发货,按快递公司通知,西藏、西藏地区的快递暂停发货。 </view>
					</view>
				</swiper-item>
				<swiper-item>
					<view class="swiper-item"></view>
				</swiper-item>
				<swiper-item>
					<view class="swiper-item"></view>
				</swiper-item>
			</swiper>
		</view>
		
		<view class="notice-text">
			公告详情公告详情公告详情公告详情公告详情公告详情公告详情公告详情公告详情公告详情公告详情公告详情公告详情
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		onShow() {
			console.log('2')
		},
		methods: {
			
		}
	}
</script>

<style>
	.notice-text{
		color: #666666;
		font-size: 28rpx;
	}
</style>
