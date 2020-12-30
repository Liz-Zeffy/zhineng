<template>
	<view class="content">	
		<status-bar/>
		<group-frame>
				<group-list slot="list"></group-list>
				<view slot="left" class="left">
					<image src="/static/images/group/video.png" alt="" mode="widthFix" />
					<text>监控视频</text>
				</view>
				<view slot="center" class="center">
					<view class="name">{{mainType}}：{{mainName}}</view>
					<image src="/static/images/group/edit_w.png" 
								 alt="" 
								 mode="widthFix"
								 @click="modifyMainName"/>
				</view>
				<view slot="right" class="right">
					<image src="/static/images/group/back.png" 
								 alt="" 
								 mode="widthFix" />
					<text>返回</text>
				</view>
		</group-frame>
		<uni-drawer class="drawer"
								ref="drawer"
								mode="right"
							 :maskClick="true">
			<view></view>				 
			<view class="top">
				<image src="/static/images/group/modify_title.png" alt="" mode="widthFix"/>
				<icon type="clear"/>
			</view>
			<view class="title"><text>柜体信息</text></view>

		</uni-drawer>
	</view>
</template>

<script>
	import GroupList from "../../components/group/GroupIist.vue"
	import StatusBar from "../../components/common/statusBar/StatusBar.vue"
	import GroupFrame from "../../components/groupFrame/GroupFrame.vue"
	import UniDrawer from "../../components/uni-drawer/uni-drawer.vue"

	export default {
		components:{
			GroupList,
			StatusBar,
			GroupFrame,
			UniDrawer
		},

		data() {
			return {
				mainType:"层架主柜",
				mainName:"柜子名称007",

			}
		},
		onLoad() {

		},
		methods: {
			modifyMainName(){
				console.log(1);
				this.$refs.drawer.open();
			}
		}
	}
</script>

<style scoped>
	.content {
		position:relative;
		width:100vw;
		height:100vh;
	}
	.left,.right {
		display: flex;
		align-items: center;
		justify-content: space-between;
		padding:0 18rpx;
		width:82rpx;
		height:26rpx;
		background:#fff;
		border-radius: 25px;
		font-size:12rpx;
		color:#61ADFF;
		font-weight: 400;
	}
	
	.left image {
		width: 22rpx;
	}
	.center {
		display: flex;
		align-items: center;
	}
	.center .name {
		font-size:15rpx;
		color: #fff;;
		margin: 0 8rpx;
	}
	.center image {
		width:11rpx;
	}
	.right {
		width:48rpx;
	}
	
	.right image {
		width: 15rpx;
		
	}
	
	.drawer .top {
		display: flex;
		align-items: center;
		justify-content:space-between;
		border:0.5px gold solid;
		height:65rpx;
	}
	.drawer .top  image {
		width:86rpx;
	}
	.drawer .top icon {
		width:23rpx;
		margin-right:21rpx;
	}
	.drawer .title{
		font-size:14rpx;
		color: #fff;
		position: absolute;
		left:0;
		top:0rpx;
		border:0.5px red dashed;
		height:65rpx;
		width:86rpx;
		display: flex;
		align-items: center;
		justify-content: center;
	}
	
	

</style>

