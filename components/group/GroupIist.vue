<template>
		<view class="group-list">
			<group-item title="综合副柜"/>
			<group-item title="层架副柜"/>
			<group-item title="挂架副柜"/>
			<group-item title="层架副柜"/>			
			<group-item title="综合副柜"/>
			<group-item title="层架副柜"/>

			<view class="add">
				<image class="bg" src="/static/images/group/add.png" alt=""  mode="widthFix"/>
			</view>
		</view>
</template>

<script>
	import GroupItem from "./GroupItem.vue"
	export default {
		name:"GroupList",
		components:{
			GroupItem,
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
.group-list {
	display: flex;
	flex-wrap:wrap;
	width:730rpx;
	justify-content: flex-start;
  /* border:0.5px red solid; */
	margin:0 auto;
	height:310rpx;
	overflow: scroll;
	padding-top:16rpx;

}
.add {
	width:127rpx;
	height:165 rpx;
	margin-left:16rpx;
	margin-bottom:11rpx
}
.bg {
	width:127rpx;
}


</style>

