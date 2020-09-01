<template>
	<div>
		<keep-alive>
			<component v-bind:is="currentCompont"></component>
		</keep-alive>
		
		<button @click="switchB()">切换b</button>
		<button @click="switchC()">切换c</button>
	</div>
</template>

<script>
	import ComponetB from "./ComponetB.vue"
	/* import ComponetC from "./ComponetC.vue" */
	const ComponetC = ()=> import("./ComponetC.vue");
	export default{
		data(){
			return {
				currentCompont:ComponetB
			}
		},
		components:{
			ComponetB,
			ComponetC
		},
		methods:{
			switchB(){
				this.currentCompont = ComponetB;
			},
			switchC(){
				this.currentCompont = ComponetC;
			}
		}
	}
</script>

<style>
</style>
