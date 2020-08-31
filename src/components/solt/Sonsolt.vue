<template>
	<div>
		this is a son solt
		<br/>
		<slot name="header">
			
		</slot>
		<slot>
			
		</slot>
		<slot name="footer" :userData="user">
			
		</slot>
		
		
	</div>
</template>

<script>
	export default{
		data(){
			return {
				user:{
					name:"林虎",
					age:10,
					heigh:181
				}
			}
		}
	}
</script>
  
<style>
</style>
