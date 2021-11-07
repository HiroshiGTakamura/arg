<script setup>
const router = useRouter();
const log = ref("");
const pass = ref("");
const err = ref(false);
const verify = {
	ver: function () {
		if (log.value.toLowerCase() == "ginasantos@gmail.com" && pass.value == "va260295") {
			// router.push("/game");
			window.location.pathname = "/game";
			err = false;
		} else {
			err.value = true;
		}
	},
};
</script>
<template>
	<Navbar />
	<div class="p-8 text-justify">
		<div class="flex items-center justify-center">
			<div class="login h-40">
				<h1>Login</h1>
				<input class="border-2 border-gray-700 rounded-sm" v-model="log" placeholder="me@email.com" />
				<h1>Senha</h1>
				<input class="border-2 border-gray-700 rounded-sm" v-model="pass" placeholder="*********" />
				<div class="flex justify-between mt-2">
					<button @click="verify.ver()" class="text-white bg-blue-500 button hover:bg-blue-600">Entrar</button>
				</div>
				<div v-if="err.valueOf()">
					<h1 class="mt-3 bg-red-300 border-2 border-red-700 rounded-md">ERRO: Login ou senha estão INCORRETOS.</h1>
				</div>
			</div>
		</div>
	</div>
</template>
