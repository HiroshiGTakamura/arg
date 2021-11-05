<template>
	<div>
		<NuxtPage />
	</div>
</template>

<style>
@tailwind base;
@tailwind components;
@tailwind utilities;
.button {
	@apply font-semibold px-2 border border-black rounded-lg text-lg;
}
.login {
	@apply bg-white border border-gray-300 rounded-md w-56 drop-shadow-lg p-3;
}
</style>
