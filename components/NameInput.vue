<template>
	<div class="flex justify-center gap-8 items-center flex-col md:flex-row p-8">
		<img class="bg-white w-32" :src="'/assets/' + imgName" />
		<input class="h-7 w-60" type="text" v-model="modelRef" />
	</div>
</template>

<script>
export default {
	props: ["imgName", "modelRef"],
};
</script>
