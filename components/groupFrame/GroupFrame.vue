<template>		
	<view class="bg_box">
		<slot name="list"></slot>
		<view class="bottomBar">
			<view class="bottomItem leftItem"><slot name="left"></slot></view>
			<view class="bottomItem centerItem"><slot name="center"></slot></view>
			<view class="bottomItem rightItem"><slot name="right"></slot></view>
		</view>
	</view>
</template>

<script>
	export default {
		name:"GroupFrame",
		components:{

		},

		data() {
			return {

			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style scoped>
	.bg_box {
		position: absolute;
		bottom:9rpx;
		left:9rpx;
		box-sizing: border-box;
		width: 730rpx;
		height: 357rpx;
		background: #FFF;
		border: 2px solid #4F9AFF;
		box-shadow: 0px 3px 8px 0px rgba(3, 28, 62, 0.24);
		border-radius: 16px;
		overflow: hidden;
	}
	.bottomBar {
		position: absolute;
		display: flex;
		flex:1;
		justify-content: space-between;
		align-items: center;
		padding:0 16rpx;
		box-sizing: border-box;
		bottom:-0.58rpx;
		left:-1.2rpx;
		width:730rpx;
		height:40rpx;
		background:#4F9AFF;
		border-bottom-right-radius:17px;
		border-bottom-left-radius:17px;
	}
	.bottomItem {
		width:33.33%;
		/* border:0.5px gold solid; */
		display: flex;
	}
	
	.centerItem {
		justify-content: center;
	}
	.rightItem {
		justify-content: flex-end;
	}
</style>
