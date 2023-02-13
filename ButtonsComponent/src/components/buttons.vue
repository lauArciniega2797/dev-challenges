<script setup>
import buttonItem from './buttonElement.vue'
import elementContainer from './element.vue'

const msg = 'Default'
const msg2 = '&:hover, &:focus'
</script>

<template>
	<div id="principal">
		<h1>Buttons</h1>
		<div>
			<elementContainer text="&lt;Button /&gt;">
				<buttonItem :message="msg" color="default"></buttonItem>
			</elementContainer>
			<elementContainer :text="msg2" class="hoverFocus">
				<buttonItem :message="msg" color="default" class="hover"></buttonItem>
			</elementContainer>
		</div>
		<div>
			<elementContainer text='&lt;Button variant="outline" /&gt;'>
				<buttonItem :message="msg" variant="outline"></buttonItem>
			</elementContainer>
			<elementContainer :text='msg2' class="hoverFocus">
				<buttonItem :message="msg" variant="outline" class="hover"></buttonItem>
			</elementContainer>
		</div>
		<div>
			<elementContainer text='&lt;Button variant="text" /&gt;'>
				<buttonItem variant="text" :message="msg" disableShadow></buttonItem>
			</elementContainer>
			<elementContainer :text='msg2' class="hoverFocus">
				<buttonItem variant="text" :message="msg" class="hover" disableShadow></buttonItem>
			</elementContainer>
		</div>
		<div>
			<elementContainer text='&lt;Button disableShadow/&gt;'>
				<buttonItem disableShadow color="primary" :message="msg"></buttonItem>
			</elementContainer>
		</div>
		<div>
			<elementContainer text='&lt;Button disabled/&gt;'>
				<buttonItem disabled message="Disabled"></buttonItem>
			</elementContainer>
			<elementContainer text='&lt;Button variant="text" disabled/&gt;'>
				<buttonItem disabled variant="text" message="Disabled" disableShadow></buttonItem>
			</elementContainer>
		</div>
		<div>
			<elementContainer text='&lt;Button startIcon="fa-user"/&gt;'>
				<buttonItem startIcon="fa-user" color="primary"></buttonItem>
			</elementContainer>
			<elementContainer text='&lt;Button endIcon="fa-heart"/&gt;'>
				<buttonItem endIcon="fa-heart" color="primary"></buttonItem>
			</elementContainer>
		</div>
		<div>
			<elementContainer text='&lt;Button size="sm"/&gt;'>
				<buttonItem size="sm" color="primary" :message="msg"></buttonItem>
			</elementContainer>
			<elementContainer text='&lt;Button size="md"/&gt;'>
				<buttonItem size="md" color="primary" :message="msg"></buttonItem>
			</elementContainer>
			<elementContainer text='&lt;Button size="lg"/&gt;'>
				<buttonItem size="lg" color="primary" :message="msg"></buttonItem>
			</elementContainer>
		</div>
		<div>
			<elementContainer text='&lt;Button color="default"/&gt;'>
				<buttonItem color="default" :message="msg"></buttonItem>
			</elementContainer>
			<elementContainer text='&lt;Button color="primary"/&gt;'>
				<buttonItem color="primary" message="primary"></buttonItem>
			</elementContainer>
			<elementContainer text='&lt;Button color="secondary"/&gt;'>
				<buttonItem color="secondary" message="secondary"></buttonItem>
			</elementContainer>
			<elementContainer text='&lt;Button color="danger"/&gt;'>
				<buttonItem color="danger" message="danger"></buttonItem>
			</elementContainer>			
		</div>
		<div>
			<elementContainer :text='msg2' class="hoverFocus">
				<buttonItem color="default" :message="msg" class="hover"></buttonItem>
			</elementContainer>
			<elementContainer>
				<buttonItem color="primary" message="primary" class="hover"></buttonItem>
			</elementContainer>
			<elementContainer>
				<buttonItem color="secondary" message="secondary" class="hover"></buttonItem>
			</elementContainer>
			<elementContainer>
				<buttonItem color="danger" message="danger" class="hover"></buttonItem>
			</elementContainer>			
		</div>
	</div>
</template>
<style scoped>
	div#principal {
		padding: 3.31em 5.18em;
	}
	div#principal > div {
		display: grid;
	    grid-auto-columns: 20em;
	    grid-auto-flow: column;
		align-items: end;
	}
	h1 {
		margin-bottom: 1.7em;
		font-weight: 500;
		line-height: 36px;
		color: #4F4F4F;
	}
</style>
