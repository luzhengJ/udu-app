<template>
	<view>
		<list-boxt :name="name" :word="word">
			<i-course-item :item="item" v-for="(item,index) in courseData" :key="item.id"></i-course-item>
		</list-boxt>
	</view>
</template>

<script>
	import listBoxt from "@/pages/index/components/list-box.vue"
	import courseData from "@/mock/courseData.js"
	import iCourseItem from "@/components/common/i-course-item.vue"
	export default {
		props:{
			name : {
				type : String,
				default : ""
			},
			word : {
				type : String,
				default : ""
			},
			courseData : {
				type : Array,
				default : () => courseData
			}
		},
		data() {
			return {
				
			};
		},
		components:{
			listBoxt,
			iCourseItem
		}
	}
</script>

<style lang="scss">

</style>
