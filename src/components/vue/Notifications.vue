
<script setup>
import { ref } from 'vue';

const counter = ref(0);

function decrement() {

	if (counter.value > 0) {
		counter.value--;
	}

}

function increment() {

	counter.value++;

}

</script>

<template>
	<div class="flex-col bg-gray-50 rounded py-8 px-6 w-96 shadow-[1px_11px_29px_1px_rgba(219,81,219,1)] flex items-center">
		<div class="relative ">
			<img class="size-40 rounded-full" src="https://art.ngfiles.com/thumbnails/2220000/2220115_full.webp?f1638560071"
				alt="" />
			<div v-show="counter > 0"
				class="flex justify-center items-center size-8 rounded-full bg-red-500 text-white absolute top-0 right-0 ">
				{{ counter }}
			</div>
		</div>
		<p v-if="counter > 0">Tienes nuevos mensajes 😘😘😘</p>
		<p v-else>Nadie te habla, pola o miedo ¿? 👍👍👍</p>
		<div class="flex justify-around w-32 mt-6">
			<button @click="decrement"
				class="bg-teal-700 text-white w-10 h-10 rounded px-2 flex justify-center items-center">-</button>
			{{ counter }}
			<button @click="increment"
				class="bg-teal-700 text-white w-10 h-10 rounded px-2 flex justify-center items-center">+</button>
		</div>

	</div>
</template>