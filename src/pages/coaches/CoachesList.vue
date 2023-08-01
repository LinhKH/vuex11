<template>
	<div></div>
</template>

<script>
export default {
	components: {},
	data() {
		return {
			isLoading: false,
			error: null,
			activeFilters: {
				frontend: true,
				backend: true,
				career: true,
			},
		};
	},
	computed: {
		filteredCoaches() {
			return this.$store.getters['coaches/coaches'];
		},
		hasCoaches() {
			return !this.isLoading && this.$store.getters['coaches/hasCoaches'];
		},
	},
};
</script>

<style scoped>
ul {
	list-style: none;
	margin: 0;
	padding: 0;
}

.controls {
	display: flex;
	justify-content: space-between;
}
</style>