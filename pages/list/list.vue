<template>
	<view>
		<view>
			<button @click="pullDown">点击刷新</button>
		</view>
		<view v-for="item in list" style="height: 300px;">{{item}}</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				list: ['前端', 'JAVA','UI','测试','大数据']
			}
		},
		onPullDownRefresh() {
			setTimeout(() =>{
				uni.request({
				    url: 'http://10.10.10.1:8887/api/Login/Login', //仅为示例，并非真实接口地址。
				    data:{
					  "UserAccount": "admin",
					  "PassWord": "123456"
					},
				    success: function (res) {
				        console.log(res.data);
				    }
				});
				this.list= ['C#','前端', 'JAVA','UI','测试','大数据']
				uni.stopPullDownRefresh()
			}, 2000)
			console.log('触发下拉刷新')
		},
		onReachBottom() {
			console.log('页面触底了')
			this.list = [...this.list, ['C#','前端', 'JAVA','UI','测试','大数据']]
		},
		methods: {
			pullDown() {
				uni.startPullDownRefresh()
			}
		}
	}
</script>

<style>

</style>
