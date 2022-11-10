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
		
		<!-- 使用热门推荐 近期上新、免费精选 、付费精品板块组件 -->
		<view class="list-container">
			<!-- 热门推荐 -->
			<swiper-course name="热门推荐" word="HOT"></swiper-course>
			<!-- 近期上新 -->
			<scoll-course name="近期上新" word="NEW"></scoll-course>
			<!-- 免费精选 -->
			<swiper-course name="免费精选" word="FREE"></swiper-course>
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
	// 引入近期上新组件
	import scollCourse from "@/pages/index/components/scroll-course.vue"
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
		components:{
			iSearchInput,
			iBanner,
			courseCategory,
			swiperCourse,
			scollCourse
		}
	}
</script>

<style lang="scss">
	.list-container{
		padding: 0 30rpx;
	}
</style>
