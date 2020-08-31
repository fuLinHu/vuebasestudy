<template>
	<div>
		this is a Soltparent
		<Sonsolt>
			<h1>uuuuu</h1>
			<h3> this is Soltparent--{{message}} </h3>
			<template v-slot:header >
				<h2 style="color: red;">this is a header</h2>
			</template>
			<!-- <template #footer="data"> -->
			<template #[soltName]="data">
				<h2 style="color: red;">
					this is a footer ===>>
					<br/>
					{{data.userData.name}}--
					<br/>
					{{data.userData.age}}--
					<br/>
					{{data.userData.heigh}}--
				</h2>
			</template>
		</Sonsolt>
	</div>
</template>

<script>
	import Sonsolt from "./Sonsolt.vue"
	export default{
		name:"Soltparent",
		components:{
			Sonsolt
		},
		data(){
			return {
				message:"这是在父模块定义的数据",
				soltName:"footer"
			}
		}
	}
</script>

<style>
</style>
