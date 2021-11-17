<script setup>
const router = useRouter();
const log = ref("");
const pass = ref("");
const err = ref(false);
const verify = function () {
	if (log.value.toLowerCase() == "jonathan.m.rodrigues07@gmail.com" && pass.value.toLowerCase() == "emergencia07") {
		// router.push("/game");
		window.location.pathname = "/game";
		err = false;
	} else {
		err.value = true;
	}
};
</script>
<template>
	<Navbar />
	<div class="flex flex-col gap-4 m-auto translate-y-1/2 login h-52">
		<div class="flex-shrink">
			<h1>Login</h1>
			<input class="w-full border-2 border-gray-700 rounded-sm" v-model="log" placeholder="me@email.com" />
		</div>
		<div class="flex-shrink">
			<h1>Senha</h1>
			<input class="w-full border-2 border-gray-700 rounded-sm" v-model="pass" placeholder="*********" />
		</div>

		<div class="flex justify-between flex-shrink mt-2">
			<button @click="verify()" class="text-white bg-blue-500 button hover:bg-blue-600">Entrar</button>
		</div>
		<div v-if="err.valueOf()">
			<h1 class="mt-3 bg-red-300 border-2 border-red-700 rounded-md">ERRO: Login ou senha estão INCORRETOS.</h1>
		</div>
	</div>
</template>
