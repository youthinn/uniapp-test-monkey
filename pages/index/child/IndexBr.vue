<template>
	<view class="index-br">
		<view class="br-img">
			<image src="../../../static/矩形27.png" mode=""></image>
		</view>

		<text>A Hairy Monkey</text>
	</view>
</template>

<script>
	export default {

	}
</script>

<style lang="scss">
	.index-br {
		margin-top: 100rpx;
		width: 100%;
		text-align: center;

		.br-img {
			width: 96%;
			margin: auto auto;
			
			image {
				width: 100%;
				height: 4rpx;
				border-radius: 6rpx;
			}
		}

		text {
			width: 100%;
			height: 200rpx;
			line-height: 200rpx;
			color: #9f9e9e;
		}
	}
</style>
