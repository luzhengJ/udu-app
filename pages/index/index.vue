<template>
	<view>
		<!-- <view class="iconfont icon-ren" style="font-size: 50px;"></view>
		<view class="iconfont" style="font-size: 50px;">&#xe607;</view> -->
		<!-- 使用搜索框组件 -->
		<!-- #ifdef MP-WEIXIN -->
		<i-search-input></i-search-input>
		<!-- #endif -->
		
		<!-- 轮播图 -->
		<i-banner></i-banner>
		
		<!-- 使用分类组件 -->
		<courseCategory></courseCategory>
		
		<!-- 使用热门推荐板块组件 -->
		<view class="list-container">
			<swiper-course></swiper-course>
		</view>
	</view>
</template>

<script>
	// 引入搜索框组件
	import iSearchInput from "@/components/common/i-search-input.vue"
    // 引入热门滚动信息模型
	import SearchModel from "@/model/searchModel.js"
	// 引入轮播图组件
	import iBanner from "@/components/common/i-banner.vue"
	// 引入分类组件
	import courseCategory from "@/pages/index/components/course-category.vue"
	// 引入热门推荐模块
	import swiperCourse from "@/pages/index/components/swiper-course.vue"
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
			iSearchInput,
			iBanner,
			courseCategory,
			swiperCourse
		}
	}
</script>

<style lang="scss">
	.list-container{
		padding: 0 30rpx;
	}
</style>
