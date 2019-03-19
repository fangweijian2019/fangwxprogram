<script>
	export default {
		onLaunch: function () {
			console.log('App Launch')
		},
		onShow: function () {
			console.log('App Show')
		},
		onHide: function () {
			console.log('App Hide')
		}
	}
</script>

<style>
	/*每个页面公共css */
	@import './common/uni.css';
	
	
	uni-page-head
    {
        display: none;
    }
	.uni-navbar-header .uni-navbar-header-btns:first-child{
		padding-left:10px !important;
		width:32px !important;
	}
	uni-checkbox .uni-checkbox-input.uni-checkbox-input-checked {
		background: #007AFF;
	}
</style>
