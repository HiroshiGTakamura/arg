<script setup>
const log = ref("");
const pass = ref("");
const pass2 = ref("");
</script>
<template>
	<Navbar />
	<div class="flex items-center justify-center">
		<div class="login h-72">
			<h1>Login</h1>
			<input class="border-2 border-gray-700 rounded-sm" v-model="log" placeholder="me@email.com" />
			<p>A mensagem é: {{ log }}</p>
			<h1>Senha</h1>
			<input class="border-2 border-gray-700 rounded-sm" v-model="pass" placeholder="*********" />
			<p>A mensagem é: {{ pass }}</p>
			<h1>Confirmar senha</h1>
			<input class="border-2 border-gray-700 rounded-sm" v-model="pass" placeholder="*********" />
			<p>A mensagem é: {{ pass }}</p>
			<div class="flex justify-between mt-2">
				<NuxtLink class="text-blue-500 underline" to="/">Voltar</NuxtLink>
				<button class="text-white bg-blue-500 button hover:bg-blue-600">Entrar</button>
			</div>
		</div>
	</div>
</template>
