<template>
	<view >
<!-- 		<view>
			<text selectable>这是信息 hello-uni</text>
		</view>
		<view>
			<text>这是信息 hello-uni</text>
		</view>
		<view>
			<text space="emsp">这是信息   hello-uni</text>
		</view>
		<view>
			<text decode>这是信息&nbsp;hello-uni</text>
		</view> -->
		<view class="box" :hover-stay-time="2000" hover-class="box-active" hover-stop-propagation="">
			盒子
		</view>
		<button size="mini" type="primary" hover-stop-propagation>按钮</button>
		<button size="mini" type="primary" disabled hover-stop-propagation>按钮</button>
		<image src="../../static/logo.png" mode="aspectFit"></image>
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

<style>
.box {
	height: 100px;
	width: 100px;
	background: green;
}
.box-active {
	background: red;
}
.box2 {
	height: 200px;
	width: 200px;
	background: blue;
}
.box2-active {
	background: black;
}
</style>
