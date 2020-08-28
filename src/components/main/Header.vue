<template>
	<div>
		<span>
			this is a header
			<span>
				this is parent to childrent--{{title}}
			</span>
		</span>
		<div>
			<button @click="sendDataToParent">这个是验证子传父的方法</button>
			<input v-model="message" />
		</div>
	</div>
</template>
	
<script>
	export default {
		name:"Header",
		props:["title"],
		data(){
			return {
				message:""
			}
		},
		methods:{
			sendDataToParent(){
				/* this.$emit("parentEvent",this.message); */
				this.$emit("update:parentEvent",this.message); 
			}
		}
	}
</script>
	
<style>
</style>
