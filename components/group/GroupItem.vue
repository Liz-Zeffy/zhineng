<template>
	
	<view class="group-item">
		<image class="bg" :src="imgURL.bg" alt=""  mode="widthFix"/>
		<text class="title">{{title}}</text>
		<image class="edit_icon" src="/static/images/group/edit_b.png" alt=""  mode="widthFix"/>
		<view class="main_icon">
			<image :src="imgURL.icon" alt="" mode="widthFix"/>
		</view>
		<view class="info">
			<view>名称</view>
			<view class="name"><text>{{name}}</text></view>
		</view>
	</view>

</template>

<script>
	export default {
		name:"GroupItem",
		props:{
			title:{
				type:String,
				default:'综合副柜'
			},
			name:{
				type:String,
				default:'副柜2121'
			}
		},
		data() {
			return {

			}
		},
		computed:{
			imgURL(){
				if(this.title == "综合副柜"){
					return {
						"bg":"/static/images/group/bg_zh.png",
						"icon":"/static/images/group/icon_zh.png"
					}
				} else if (this.title == "层架副柜"){
					return {
						"bg":"/static/images/group/bg_cj.png",
						"icon":"/static/images/group/icon_cj.png"
					}
				} else { 
					return {
						"bg":"/static/images/group/bg_gj.png",
						"icon":"/static/images/group/icon_gj.png"
					}
				}
			},

		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style scoped>

	.group-item{
		position: relative;
		width:127rpx;
		height: 165rpx;
		margin-left:16.5rpx;
		margin-bottom:11rpx
	}
	.bg {
		width: 127rpx;
	
	}
	.title {
		position: absolute;
		left: 14.5rpx;
		top:6rpx;
		font-size: 11rpx;
		color:#fff;
	}
	.edit_icon {
		position: absolute;
		top:8rpx;
		right:13rpx;
		width:11rpx;
	}
	.main_icon {
		position: absolute;
		background:#fff;
		padding:14rpx 32rpx 8rpx;
		top:31px;
		left:14rpx;
		border-radius: 5rpx;
	}
	
	.main_icon image {
		width:35rpx;
		heigth:48rpx;
		
	}
	.info {
		position: absolute;
		bottom:14rpx;
		text-align: center;
		width:100%;
	}
	.info > view {
		font-size: 6rpx;
		color:#777;
	}
	
	.info .name {
		font-size: 12rpx;
		color: #333;
	}

</style>

