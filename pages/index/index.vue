<template>
	<view class="content">
		<index-title />
		<index-text :title="title1" :content="content1" />
		<slide-img :slideImg="slideImg1" @getPosition="getPosition" :slidePosition="slidePosition" />
		<index-br />
		<view class="bth">
			<button>STRANGERS</button>
		</view>
		<slide-img :slideImg="slideImg2" @getPosition="getPosition" :slidePosition="slidePosition" />
		<index-text :title="title2" :content="content2" />
		<slide-img :slideImg="slideImg3" @getPosition="getPosition" :slidePosition="slidePosition" />
		<slide-img :slideImg="slideImg4" @getPosition="getPosition" :slidePosition="slidePosition" />
		<!-- 图片反向滑动：获取总长度 减去 获取当前滑动位置 -->
		<!-- <slide-img :slideImg="slideImg4" @reverse="reverse - getPosition" :slidePosition="slidePosition" /> -->
		<index-text :title="title3" :content="content3" />
		<index-text :title="title4" :content="content4" />
		<index-text :title="title5" :content="content5" />
		<index-br />
	</view>
</template>

<script>
	import IndexTitle from './child/IndexTitle.vue'
	import IndexText from '@/component/indextext/IndexText.vue'
	import IndexBr from './child/IndexBr.vue'
	import SlideImg from '@/component/slideimg/SlideImg.vue'

	export default {
		data() {
			return {
				title1: 'A Hairy Monkey',
				content1: 'Hairy Monkey is a unique collection that combines scary fun with funny. Emei Mountain dances with goldenmonkeys,and your Bored Ape can double as your membership card and grant exclusive benefits to members. Oh,honey, this is great.',
				title2: 'Project Details Team',
				content2: 'NFT is developed by the DAO organization formed by overseas blockchain enthusiasts and is strongly supported and funded by well-known investment institutions.',
				title3: 'Mission',
				content3: 'Decentrally distributed interests are given to the community,allowing participants to have more transparent governance rights and dividend rights so that all the efforts can be rewarded.All the love and enthusiasm can be respected and rewarded with a promising return. ',
				title4: 'Partner',
				content4: 'A Hairy Monkey NFT has been certified and funded by Hollywood Metaverse Ecological Group,American Sunshine Hedge Fund,Global Capital and many other investment institutions,providing multiple resources for the development of the project and escorting the sustainable progress of the project Thanks to the support of these potent institutions, the community is expected to have rapid growth. ',
				title5: 'Prospect',
				content5: 'Based on the advancement of encryption infrastructure,the wider recognition of NFTs, and the goal of deeper creativity,aim at becoming one of the largest NFT trading platforms! A Hairy Monkey',
				slideImg1: [{
					src: require('@/static/11.png'),
				}, {
					src: require('@/static/12.png'),
				}, {
					src: require('@/static/13.png'),
				}, {
					src: require('@/static/14.png'),
				}, {
					src: require('@/static/15.png'),
				}, {
					src: require('@/static/16.png'),
				}],
				slideImg2: [{
					src: require('@/static/2-1.png'),
				}, {
					src: require('@/static/2-2.png'),
				}, {
					src: require('@/static/2-3.png'),
				}, {
					src: require('@/static/2-4.png'),
				}, {
					src: require('@/static/2-5.png'),
				}, {
					src: require('@/static/2-6.png'),
				}],
				slideImg3: [{
					src: require('@/static/3-1.png'),
				}, {
					src: require('@/static/3-2.png'),
				}, {
					src: require('@/static/3-3.png'),
				}, {
					src: require('@/static/3-4.png'),
				}, {
					src: require('@/static/3-5.png'),
				}],
				slideImg4: [{
					src: require('@/static/3-5.png'),
				}, {
					src: require('@/static/3-4.png'),
				}, {
					src: require('@/static/3-3.png'),
				}, {
					src: require('@/static/3-2.png'),
				}, {
					src: require('@/static/3-1.png'),
				}],
				slidePosition: 100
			}
		},
		components: {
			IndexTitle,
			IndexText,
			IndexBr,
			SlideImg,
		},
		onLoad() {
		},
		methods: {
			getPosition(x) {
				this.slidePosition = x
				// setTimeout(() => this.slidePosition = x, 1000)
			}
		},
		computed: {
			reverse() {
				return this.slideImg4.length * 150 
			}
		}
		
	}
</script>

<style lang="scss">
	.content {
		width: 100%;
		height: 5660rpx;
		background-color: #202023;

		.bth {

			button {
				border: none;
				background-color: #343434;
				width: 500rpx;
				font-size: 28rpx;
				color: #9d9c9c;
			}

		}
	}
</style>
