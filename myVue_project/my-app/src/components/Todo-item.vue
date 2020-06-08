<template>
	<li class='item'>{{item}}</li>
</template>
<script>
	
export default {
  name: 'To-item',
  props: {
    item: String
  }
}
</script>

<style>
	.item{
		color: red;
		font-size: 15px;
	}
</style>
