<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		}
	}
</script>

<style>
	/*每个页面公共css */
	/**
	 * 引入公共样式
	 */
	@import url("@/common/css/common.css");
	/**
	 * 引入字体图标
	 */
	@import url("~@/static/icon/iconfont.css");
</style>
