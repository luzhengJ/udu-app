<template>
	<view class="search-box">
		<input type="text" class="search-input" placeholder="请输入你想要的内容">
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			};
		}
	}
</script>

<style lang="scss">
.search-box{
	width: 100%;
	position: absolute;
	left: 0;
	top: 30rpx;
	z-index: 9999;
	.search-input{
		height: 70rpx;
		line-height: 40rpx;
		border-radius: 30rpx;
		text-align: center;
		background-color:  #f8f8f8;
		margin: 0 20rpx;
	}
}
</style>
