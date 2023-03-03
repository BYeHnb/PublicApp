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
			//写一个方法，判断邮箱格式是否正确
			isEmail(str) {
				var reg = /^([a-zA-Z0-9_-])+@([a-zA-Z0-9_-])+(.[a-zA-Z0-9_-])+/
				return reg.test(str)
			},
			//写一个方法，判断手机号码格式是否正确
			isPhoneNum(str) {
				var reg = /^1[3|4|5|7|8][0-9]{9}$/
				return reg.test(str)
			},
			//写一个方法，判断身份证号码格式是否正确
			isIdCard(str) {
				var reg = /(^\d{15}$)|(^\d{18}$)|(^\d{17}(\d|X|x)$)/
				return reg.test(str)
			},
			//写一个方法，判断是否是数字
			isNumber(str) {
				var reg = /^[0-9]*$/
				return reg.test(str)
			},
			//写一个方法，判断是否是中文
			isChinese(str) {
				var reg = /^[\u4e00-\u9fa5]{0,}$/
				return reg.test(str)
			},
			//写一个方法，判断是否是字母
			isLetter(str) {
				var reg = /^[a-zA-Z]+$/
				return reg.test(str)
			},
			//写一个方法，判断是否是字母和数字
			isLetterAndNumber(str) {
				var reg = /^[a-zA-Z0-9]+$/
				return reg.test(str)
			},
			//发送请求，获取数据并渲染JSON数据
			getData() {
				uni.request({
					url: 'https://www.easy-mock.com/mock/5c1dfd98e8bfa547414a5278/baixing/dabaojian',
					success: (res) => {
						console.log(res)
					}
				})
			},


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
