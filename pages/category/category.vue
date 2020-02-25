<template>
	<uni-list>
		<uni-list-item @click="goto(11)" v-for="i in 5" :key="i" :title="i" /> 
	</uni-list>
</template>

<script>
	export default {
		data() {
			return {

			}
		},
		methods: {
			goto(id){
				console.log(id)
				uni.navigateTo({
				    url: '../postList/postList?id=' + id
				});
			}
		}
	}
</script>

<style>

</style>
