<template>
	<view class="course-item">
		<view class="item-left">
			<image class="course-cover" :src="item.mainImage"></image>
			<view class="course-time">
				{{item.totalTime}}
			</view>
		</view>
		<view class="item-right">
			<view class="title text-ellipsis">{{item.title}}</view>
			<view class="info">
				<view class="nickname iconfont icon-laoshi2">{{item.nickName}}</view>
				<view class="count">
					<view v-if="item.isFree === 1" class="money iconfont icon-moneybag">免费</view>
				  <view v-else class="money iconfont icon-moneybag">
					{{item.priceOriginal || item.priceDiscount}}
				  </view>
					<view class="iconfont icon-video">{{item.studyTotal}}人在学</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default{
		props:{
			item : {
				type : Object,
				default : () => {
					return {
						id: 1,
						mainImage: 'http://10.idqqimg.com/qqcourse_logo_ng/ajNVdqHZLLAWb3qFGBhykjmcTvz9CWmwib2Qj7c3Vxjia4y5fgSoNdrMYIdH11Dl1OCraibA7u0mts/600',
						totalTime: '00:59:08',
						title: 'SpringBoot项目实战教程SpringCloud OAuth2 Vue分布式微服务架构',
						nickName: '梦老师1', // 课程老师
						isFree: 0, //是否免费：0收费，1免费
						priceOriginal: 999, // 原价
						priceDiscount: 699.9, // 优惠价
						studyTotal: 899
					}
				}
			}
		}
	}
</script>

<style lang="scss">
.course-item{
	display: flex;
	padding: 20rpx 0;
	border-bottom: 1rpx solid #F1F1F1;
	
	.item-left{
		width: 290rpx;
		height: 160rpx;
		position: relative;
		margin-right: 20rpx;
		overflow: hidden;
		
		.course-cover{
			width: 100%;
			height: 100%;
			border-radius: 10rpx;
		}
		.course-time{
			position: absolute;
			right : 5rpx;
			bottom : 5rpx;
			color : #fff;
			background-color: rgba(0,0,0,0.8);
			border-radius: 20rpx;
			font-size: 22rpx;
			padding :0 6px;
		}
	}
	
	.item-right{
		height: 160rpx;
		justify-content: space-between;
		padding-left: 5rpx;
		padding-top: 5rpx;
		overflow: hidden;
		.title{
			max-width: 365rpx;
			height: 70rpx;
			line-height: 35rpx;
			font-size: 28rpx;
			font-weight: bold;
		}
		
		.info{
			display: flex;
			flex-direction: column;
			
			.nickname {
				font-size: 23rpx;
				color: #999;
				margin: 20rpx 0 8rpx 0;
			}
			
			.count{
				display: flex;
				align-items: center;
				.iconfont{
					font-size: 23rpx;
					color: #222222;
				}
				.money{
					font-size: 28rpx;
					color: $i-color-orange;
					margin-right: 30rpx;
				}
			}
		}
	}
}
</style>