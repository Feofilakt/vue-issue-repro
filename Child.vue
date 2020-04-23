<template>
	<div>{{ a.length }}</div>
</template>

<script>
	export default {
		data: function() {
			return {
				a: []
			};
		},
		created: function() {
			for (var i = 0; i < 50000; i++) {
				this.a.push({
					b: 1,
					c: 2,
					d: 3,
					e: 4
				});
			}
		}
	};
</script>