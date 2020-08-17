<template>
	<view class="container">
		<!-- 搜索框 -->
		<uni-search-bar bgColor="#ffffff" placeholder="搜索商品" :radius="100" @confirm="search"></uni-search-bar>

		<!-- 轮播图 -->
		<carousel :img-list="imgList" url-key="url" @selected="selectedBanner" />
	</view>
</template>

<script>
	// 导入组件
	import uniSearchBar from '@/components/uni-search-bar/uni-search-bar.vue'
	import carousel from '@/components/vear-carousel/vear-carousel'
	export default {
		data() {
			return {
				imgList: [{
					url: 'https://img9.51tietu.net/pic/2019-091200/vgkpidei2tjvgkpidei2tj.jpg',
					id: 1
				}, {
					url: 'https://img9.51tietu.net/pic/2019-091200/euzekmi5m23euzekmi5m23.jpg',
					id: 2
				}, {
					url: 'https://img9.51tietu.net/pic/2019-091200/143tt0ta4sr143tt0ta4sr.jpg',
					id: 3
				}, {
					url: 'https://img9.51tietu.net/pic/2019-091200/ff1vqwm3q33ff1vqwm3q33.jpg',
					id: 4
				}]
			}
		},
		components: {
			uniSearchBar,
			carousel
		},
		methods: {
			selectedBanner(item, index) {
				console.log('🥒', item, index)
			}
		}
	}
</script>

<style lang="scss">
	.container {
		width: 100%;
		height: 100%;
		background-color: #FFFFFF;

	}
</style>
