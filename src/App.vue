<template>
	<h1>{{text}}</h1>
	<button @click="increment">Increment</button>
</template>

<script>
import {computed, ref} from 'vue';
export default {
	setup() {
		const counter = ref(0);
		const increment = () => {
			counter.value += 1;
		}
		const text = computed(()=> {
			return 'Counter: ' + counter.value;
		});
		return {
			counter,
			increment,
			text
		};
	},
}
</script>