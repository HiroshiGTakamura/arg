<script setup>
const drop = ref(false);
</script>
<template>
	<div class="fixed flex items-center justify-between w-full h-20 p-10 bg-white border-b border-gray-300 drop-shadow-lg">
		<div>(logo aqui)</div>
		<div class="flex mr-2 text-lg">
			<button @click="drop = !drop" class="flex p-1 hover:bg-gray-200">
				<h1 v-if="drop == false" class="m-2">◄ Gina Santos</h1>
				<h1 v-if="drop" class="m-2">► Gina Santos</h1>
				<p class="p-4 m-1 border-2 border-black rounded-full"></p>
			</button>
			<div v-if="drop" class="flex bg-white">
				<NuxtLink @click="drop = false" class="drop-item" to="/home">Home</NuxtLink>
				<NuxtLink @click="drop = false" class="drop-item" to="/users/ginasantos">Meu Espaço</NuxtLink>
			</div>
		</div>
	</div>
	<div class="pt-20"></div>
</template>
<style scoped>
.drop-item {
	@apply transform hover:-translate-y-1 transition-transform px-4 py-2 text-left font-semibold bg-white hover:bg-gray-200;
}
</style>
