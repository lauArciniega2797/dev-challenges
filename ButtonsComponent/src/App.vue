<script setup>
    import sidebarInput from './components/sidebar.vue';
    import buttons from './components/buttons.vue';
</script>

<template>
  <main>
    <sidebarInput></sidebarInput>

    <buttons></buttons>
  </main>
</template>

<style scoped>
	main {
		display:grid;
		grid-template-columns: 237px 1fr
	}
</style>