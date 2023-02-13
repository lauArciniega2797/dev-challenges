<template>
	<ul id="sidebar">
		<div>
			<li><span>Dev</span><span>challenges.io</span></li>
		</div>
		<div>
			<li @click="clicked">Colors</li>
			<li @click="clicked">Typography</li>
			<li @click="clicked">Spaces</li>
			<li @click="clicked" class="active">Buttons</li>
			<li @click="clicked">Inputs</li>
			<li @click="clicked">Grid</li>
		</div>
	</ul>
</template>

<script setup>
	function clicked(evt) {
		let others = evt.target.parentNode.closest('div').childNodes
		others.forEach(element => {
			element.classList.remove('active')
		})
		
		evt.target.classList.toggle('active')
	}
</script>
<style scoped>
	main #sidebar {
		background-color: #faf8fd;
		list-style-type: none;
		display: grid;
		grid-template-rows: 5vh 1fr;
		padding-left: 2.3em;
		padding-top:2.9em;
		position: sticky;
		top: 0;
		height: 100vh;
	}
	main #sidebar > div {
		display: flex;
		align-items: center;
	}
	main #sidebar > div:last-child {
		flex-direction: column;
		padding-top: 7.6em;
		align-items:unset;
	}
	main #sidebar >div:last-child li {
		color: hsla(0, 0%, 62%, 1);
		font-weight: 500;
		font-size: 1em;
		margin: 1em;
		cursor: pointer;
		transition: color .2s
	}
	main #sidebar >div:last-child li.active {
		color: hsla(231, 69%, 11%, 1);
	}
	main #sidebar li span {
		font-weight: 600;
		font-size: 1.1em;	
	}
	main #sidebar li span:first-child {
		color: hsla(11, 93%, 57%, 1);
	}
	main #sidebar li span:last-child {
		color: hsla(231, 69%, 11%, 1);
	}
</style>