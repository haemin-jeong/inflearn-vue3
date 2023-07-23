<template>
	<div>
		<div :style="styleObject">
			Lorem ipsum dolor sit amet consectetur adipisicing elit. Neque, veritatis
			impedit et aut culpa omnis dolores accusamus iure dolore mollitia, maiores
			reiciendis dolorum perspiciatis sapiente, minima consectetur. Ut, alias
			temporibus.
		</div>
		<button v-on:click="fontSize--">-</button>
		<button v-on:click="fontSize++">+</button>
	</div>
</template>

<script>
import { computed, reactive, ref } from 'vue';

export default {
	setup() {
		// const styleObject = reactive({
		// 	color: 'red',
		// 	fondSize: '13px',
		// });
		const fontSize = ref(13);
		const styleObject = computed(() => {
			return {
				color: 'red',
				fontSize: fontSize.value + 'px',
			};
		});
		return { styleObject, fontSize };
	},
};
</script>

<style lang="scss" scoped></style>
