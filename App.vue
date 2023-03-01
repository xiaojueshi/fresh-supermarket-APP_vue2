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
	page{
		background-color: #F8F9FA;
	}
	
	*{
		box-sizing: border-box;
		padding: 0;
		margin: 0;
	}
	
	.flex-center{
		display: flex;
		justify-content: center;
		align-items: center;
	}
</style>
