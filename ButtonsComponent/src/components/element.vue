<script setup>
	defineProps({
		text: String
	})
</script>
<template>
	<div>
		<span>{{ text }}</span>
		<slot></slot>
	</div>
</template>
<style scoped>
	div {
		display:flex;
		flex-direction: column;
		margin-bottom: 2.82em
	}
	div.hoverFocus span {
		font-weight: 400;
		color: #828282;
	}
	span {
		display: inline-block;
		color: #333333;
    	margin-bottom: 0.75em;
		font-weight: 400;
	}
</style>