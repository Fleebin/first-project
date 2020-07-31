<template>
	<div>
		<input @keyup.enter="onInput" placeholder="Pesquisar" />
	</div>
</template>

<script>
export default {
	name: 'SearchBar',
	methods: {
		onInput: function(e) {
			this.$emit('searchTermChange', e.target.value);
		}
	}
};
</script>

<style scoped>


	input {
		
		width: 30%;

		border-radius: 6px;
		border: 1px solid #4DCDCC;
		padding: 12px;

		outline: none;
		
	}
	div {
		text-align: center;
		margin: 5%;
	}
	input::placeholder{
		align-items: center;
	}
</style>