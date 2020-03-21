<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide') 
		}
	}
</script>

<style>
	@import url("./style/index.css");
	/*每个页面公共css */
	
	.page,html,body{
		height: 100%;
		width: 100%;
		position: absolute;
		background-color: #efefef;
		font-weight: bold;
		margin: 0rpx;
		padding: 0rpx;
	}
	
	.full{
		width: 100%;
	}
	
	.top-bg{
		width: 750rpx;
		height: 160rpx;
		background: #e9ae43;
	}
</style>
