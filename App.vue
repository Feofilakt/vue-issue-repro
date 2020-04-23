<template>
	<div id="app">
		<input type="checkbox" id="checkbox" v-model="enabled" />
		<label for="checkbox">{{ enabled ? "turn off" : "turn on" }}</label>

		<child v-if="enabled" />
	</div>
</template>

<script>
	import Child from "./Child.vue";

	export default {
		name: "App",
		components: { Child },
		data: function() {
			return {
				enabled: false
			};
		}
	};
</script>