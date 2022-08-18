<template>
	<view class="index-ahairy">
		<view class="title">
			<h1>{{ title }}</h1>
		</view>
		<view class="content">
			<text>{{ content }}</text>
		</view>
	</view>
</template>

<script>
	export default {
		props: ['title', 'content'],
	}
</script>

<style lang="scss">
	.index-ahairy {
		text-align: center;
		width: 100%;
		margin-top: 100rpx;
		color: #e6e6e6;

		.title {
			font-size: 48rpx;
		}

		.content {
			width: 84%;
			margin: 40rpx auto;
			text-align: left;

			text {
				color: #9f9e9e;
				font-size: 28rpx;
			}
		}
	}
</style>
