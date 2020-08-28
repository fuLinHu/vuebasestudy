<template>
	<div>
		i am a main
		<!-- <Header @parentEvent="getMessage"   title="这是父组件传递给子组件的内容" /> -->
		<!-- <Header @parentEvent="data=>sonData =data "   title="这是父组件传递给子组件的内容" /> -->
		<!-- <Header @update:parentEvent="data=>sonData =data "   title="这是父组件传递给子组件的内容" /> -->
		<Header :parentEvent.sync="sonData"   title="这是父组件传递给子组件的内容" />
		<div>
			this is son send data to me--{{sonData}}
		</div>
	</div>
</template>

<script>
	import Header from "./Header.vue"
	export default {
		name:"Main",
		data(){
			return{
				sonData:""
			}
		},
		components: {
		  Header
		},
		methods:{
			getMessage(data){
				this.sonData = data;
			}
		}
	}
</script>

<style>
	
</style>
