<template>
	<view>
		<postList/>
		<uni-load-more :status="more"></uni-load-more>
	</view>
</template>

<script>
	import postList from '../../components/post-list/post-list.vue'
	export default {
		components:{postList},
		data() {
			return {
				more:'loading', // loading 的状态，可选值：more（loading前）、loading（loading中）、noMore（没有更多了）
			}
		},
		methods: {
			
		}
	}
</script>

<style>

</style>
