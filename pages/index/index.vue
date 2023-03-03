<template>
	<view class="container">
		// 1.0.0版本开始，支持使用uni-link组件，可以在小程序端使用open-type属性
		<uni-link :href="href" open-type="navigate">
			<view>uni-link组件</view>
		</uni-link>
		// 写一个a标签，可以在小程序端使用open-type属性

		<a :href="href" open-type="navigate">
			<view>a标签</view>
		</a>
		// 写一个view标签，可以在小程序端使用open-type属性
		
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				href: 'https://uniapp.dcloud.io/component/README?id=uniui'
			}
		},
		methods: {

		}
	}
</script>

<style>
	.container {
		padding: 20px;
		font-size: 14px;
		line-height: 24px;
	}
</style>
