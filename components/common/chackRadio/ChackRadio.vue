<template>
	<view class="radio">
		<view class="chack">
			
		</view>
	</view>
</template>

<script>
	
	export default {
		name:"ChackRadio",
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
	.radio {
		width: 15rpx;
		height:15rpx;
		border-radius: 50%;
		border:1.2rpx solid #4F9AFF;
		display:flex;
		justify-content: center;
		align-items: center;
		box-sizing: border-box;
	}
	.chack {
		width:8rpx;
		height:8rpx;
		border-radius: 50%;
		background: linear-gradient(0deg, rgba(114, 180, 255, 0.8), rgba(73, 153, 235, 0.8), rgba(43, 125, 209, 0.8));
		box-shadow: 0px 0px 0.58rpx 0px rgba(27, 67, 140, 0.5);
		box-sizing: border-box;
	}
</style>

