<template>
	<view class="list-box">
		<view class="title row space-between">
			<view class="center">
				<text class="name">{{name}}</text>
				<text class="word">{{word}}</text>
			</view>
			<view class="all">
                 <text>全部</text>
				 <text class="iconfont icon-right"></text>
			</view>
		</view>
		<!-- 课程列表区域 --> 
		<slot></slot>
	</view>
</template>

<script>
	export default {
		props:{
			name : {
				type : String,
				default : ''
			},
			word : {
				type : String,
				default : ''
			}
		},
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="scss">
  .list-box{
	  margin-top: 60rpx;
	  
	  .name{
		  font-size: 38rpx;
		  font-weight: 500;
		  color: #303133;
		  margin-right: 10rpx;
	  }
	  
	  .word{
		  color: #fff;
		  font-size: 20rpx;
		  padding: 0 10rpx;
		  border-radius: 30rpx 30rpx 30rpx 0;
		  background-image: linear-gradient(to right,  $i-color-orange, $i-text-color-red);
	  }
	  
	  .all{
		  font-size: 28rpx;
		  color: $i-text-color-grey;
		  font-weight: normal;
		  .iconfont{
			  font-size: 20rpx;
		  }
	  }
  }
</style>
