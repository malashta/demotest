<template>
  <form class="search-bar" @submit.prevent="$emit('query', queryStr)">
    <input type="text" v-model="queryStr" :placeholder="placeholderTxt">
  </form>
</template>

<script>
export default {
  props: {
		placeholderTxt: {
			type: String
		}
  },
	data() {
		return {
			queryStr: ''
		};
	}
};
</script>

<style lang="scss">
  @import "search-bar";
</style>
