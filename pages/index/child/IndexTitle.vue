<template>
	<view class="">
		<view class="hello">
			<view class="hello-img">
				<image src="../../../static/组272.png" mode=""></image>
			</view>
			<button>Connect Wallet</button>
		</view>
	</view>
</template>

<script>
</script>

<style lang="scss">
	.hello {
		width: 100%;
		height: 80rpx;
		line-height: 80rpx;
		display: flex;
		background-image: linear-gradient(#141414, #49494c);
		.hello-img {
			// width: 300rpx;
			flex: 1;
			text-align: center;
	
			image {
				width: 240rpx;
				height: 40rpx;
				margin: auto auto;
				text-align: center;
				vertical-align: middle;
			}
		}
		button {
			position: absolute;
			top: 30rpx;
			right: 20rpx;
			font-size: 8rpx;
			color: #707070;
			width: 240rpx;
			height: 40rpx;
			line-height: 40rpx;
			text-align: center;
			background: none;
			border: 1px solid #707070;
		}
	}
</style>