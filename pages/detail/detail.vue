<template>
	<view>
		{{ title }}
		<view v-for="item in list">{{ item.name }}</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: '数据绑定学习',
				list: [
					{id: '111',name: 'eve'},
					{id: '222',name: 'tom'}
				]
			}
		},
		methods: {
			
		}
	}
</script>

<style>

</style>
