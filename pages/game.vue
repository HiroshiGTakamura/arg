<script setup>
const router = useRouter();
const name1 = ref("");
const name2 = ref("");
const name3 = ref("");
const name4 = ref("");
const name5 = ref("");
const name6 = ref("");
const name7 = ref("");

const verify = function () {
	const nameFields = [name1, name2, name3, name4, name5, name6, name7];
	const names = ["pvc", "pp", "ps", "outros", "pead", "pet", "pebd"];
	for (let i = 0; i < nameFields.length; i++) {
		if (nameFields[i].value.toLowerCase() != names[i]) {
			console.log("incorreto");

			return;
		}
	}

	console.log("correto");
};
</script>
<template>
	<title>...</title>
	<div class="flex flex-col h-full w-full align-center bg-black">
		<div class="flex justify-center gap-8 items-center flex-col md:flex-row p-8">
			<img class="bg-white w-32" src="~/assets/tile000.png" />
			<input class="h-7 w-60" type="text" v-model="name1" />
		</div>
		<div class="flex justify-center gap-8 items-center flex-col md:flex-row p-8">
			<img class="bg-white w-32" src="~/assets/tile001.png" />
			<input class="h-7 w-60" type="text" v-model="name2" />
		</div>
		<div class="flex justify-center gap-8 items-center flex-col md:flex-row p-8">
			<img class="bg-white w-32" src="~/assets/tile002.png" />
			<input class="h-7 w-60" type="text" v-model="name3" />
		</div>
		<div class="flex justify-center gap-8 items-center flex-col md:flex-row p-8">
			<img class="bg-white w-32" src="~/assets/tile003.png" />
			<input class="h-7 w-60" type="text" v-model="name4" />
		</div>
		<div class="flex justify-center gap-8 items-center flex-col md:flex-row p-8">
			<img class="bg-white w-32" src="~/assets/tile004.png" />
			<input class="h-7 w-60" type="text" v-model="name5" />
		</div>
		<div class="flex justify-center gap-8 items-center flex-col md:flex-row p-8">
			<img class="bg-white w-32" src="~/assets/tile005.png" />
			<input class="h-7 w-60" type="text" v-model="name6" />
		</div>
		<div class="flex justify-center gap-8 items-center flex-col md:flex-row p-8">
			<img class="bg-white w-32" src="~/assets/tile006.png" />
			<input class="h-7 w-60" type="text" v-model="name7" />
		</div>

		<button @click="verify()" class="text-black bg-white button hover:bg-gray-300 w-36 self-center m-8 p-3">Enviar</button>
	</div>
</template>
