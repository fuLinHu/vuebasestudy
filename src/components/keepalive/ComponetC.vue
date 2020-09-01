<template>
	<div>
		this is a C ---{{message}}
		<button @click="getmessage()">获取信息</button>
	</div>
</template>

<script>
	export default{
		data(){
			return {
				message :""
			}
		},
		methods:{
			getmessage(){
				this.message = 'this is C com message'
			}
		}
	}
</script>

<style>
</style>
