<template>
	<view class="slide-one">
		<scroll-view 
			scroll-x="true"
			class="main-scroll" 
			:scroll-left="slidePosition || reverse" 
			lower-threshold="30" 
			@scrolltolower="origin" 
			scroll-with-animation="true"
			@scroll="getPosition"
			>
			<view class="item-img"  v-for="item in slideImg" >
				<image :src="item.src" mode=""></image>
			</view>
		</scroll-view>
	</view>
</template>

<script>
	export default {
		props: ['slideImg', 'slidePosition', 'reverse'],
		methods: {
			origin() {
				this.positions = 0
			},
			getPosition(event) {
				this.$emit('getPosition', event.detail.scrollLeft)
			}
		}
	}
</script>

<style lang="scss">
	.slide-one {
		margin-top: 80rpx;
		width: 100%;
		max-width: 100%;
		display: flex;

		.main-scroll {
			width: 100%;
			height: 400rpx;
			overflow: hidden;
			white-space: nowrap;

			::-webkit-scrollbar {
				display: none;
			}

			.item-img {
				width: 300rpx;
				height: 400rpx;
				padding-left: 20rpx;
				display: inline-block;

				image {
					width: 100%;
					height: 100%;
				}


			}
		}

	}
</style>
