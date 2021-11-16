<script setup>
/*enigmas completos:
1 PVC    (3)   <-
2 PP     (5)   <-
3 PS     (6)
4 Outros (7)
5 PEAD   (2)   <-
6 PET    (1)   <-
7 PEBD   (4)   <-
*/
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
	const names = [
		"policloreto de vinila",
		"polipropileno",
		"poliestireno",
		"outros",
		"polietileno de alta densidade",
		"polietileno tereftalato",
		"polietileno de baixa densidade",
	];
	for (let i = 0; i < nameFields.length; i++) {
		if (nameFields[i].value.toLowerCase() != names[i]) {
			console.log("incorreto");
			return;
		}
	}
	router.push("/carta");
	/*console.log("correto");*/
};

function popup() {
	alert("https://imgur.com/a/--- -. -.-- --.. ...- ..-. --- \n AaaaAAA");
}

const viewing = ref(false);
</script>
<template>
	<title>...</title>
	<div class="flex flex-col w-full h-full bg-black align-center">
		<div class="flex flex-col items-center justify-center gap-8 p-8 md:flex-row">
			<a href="https://imgur.com/a/KPkf4TJ" target="_blank">
				<img class="w-32 bg-white" src="~/assets/tile000.png" />
			</a>
			<input class="font-bold h-7 w-60" type="text" v-model="name1" />
		</div>
		<div class="flex flex-col items-center justify-center gap-8 p-8 md:flex-row">
			<a href="https://imgur.com/a/NmgguZa" target="_blank">
				<img class="w-32 bg-white" src="~/assets/tile001.png" />
			</a>
			<input class="font-bold h-7 w-60" type="text" v-model="name2" />
		</div>
		<div class="flex flex-col items-center justify-center gap-8 p-8 md:flex-row">
			<NuxtLink to="/mirror" target="_blank">
				<img class="w-32 bg-white" src="~/assets/tile002.png" />
			</NuxtLink>
			<input class="font-bold h-7 w-60" type="text" v-model="name3" />
		</div>
		<div class="flex flex-col items-center justify-center gap-8 p-8 md:flex-row">
			<a href="" target="_blank">
				<img class="w-32 bg-white" src="~/assets/tile003.png" />
			</a>
			<input class="font-bold h-7 w-60" type="text" v-model="name4" />
		</div>
		<div class="flex flex-col items-center justify-center gap-8 p-8 md:flex-row">
			<button @click="popup()">
				<img class="w-32 bg-white" src="~/assets/tile004.png" />
			</button>
			<input class="font-bold h-7 w-60" type="text" v-model="name5" />
		</div>
		<div class="flex flex-col items-center justify-center gap-8 p-8 md:flex-row">
			<a href="https://imgur.com/a/wcdCjMO" target="_blank">
				<img class="w-32 bg-white" src="~/assets/tile005.png" />
			</a>
			<input class="font-bold h-7 w-60" type="text" v-model="name6" />
		</div>
		<div class="flex flex-col items-center justify-center gap-8 p-8 md:flex-row">
			<a href="https://imgur.com/a/imBxm1m" target="_blank">
				<img class="w-32 bg-white" src="~/assets/tile006.png" />
			</a>
			<input class="font-bold h-7 w-60" type="text" v-model="name7" />
		</div>

		<button @click="verify()" class="self-center p-3 m-8 text-black bg-white button hover:bg-gray-300 w-36">Enviar</button>

		<div class="items-start p-2">
			<button v-if="viewing == false" @click="viewing = !viewing" class="px-20 py-2 text-black bg-black">a</button>
			<p class="text-white" v-if="viewing">oneritseilop</p>
		</div>
	</div>
</template>
