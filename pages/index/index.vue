<template>
	<view>
		<!-- <view class="iconfont icon-ren" style="font-size: 50px;"></view>
		<view class="iconfont" style="font-size: 50px;">&#xe607;</view> -->
		<!-- 使用搜索框组件 -->
		<!-- #ifdef MP-WEIXIN -->
		<i-search-input></i-search-input>
		<!-- #endif -->
		
		
		<!-- 使用分类组件 -->
		<!-- <category-box></category-box> -->
	</view>
</template>

<script>
	// 引入搜索框组件
	import iSearchInput from "@/components/common/i-search-input.vue"
    // 引入热门滚动信息模型
	import SearchModel from "@/model/searchModel.js"
	// import categoryBox from "@/components/category-box/category-box.vue"
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {
            // #ifdef APP-PLUS
			SearchModel.handleUpdatePlaceholderText(this)
			// #endif
		},
		methods: {

		},
		components:{
			iSearchInput
			// categoryBox
		}
	}
</script>

<style>
	
</style>
