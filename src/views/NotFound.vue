<template>
	<h1>404</h1>
	<h3>Whooops that should not have happend</h3>
	<p>Be carfull this is uncharted territory</p>
	<div class="home">
		<router-link :to="{ name: 'Home' }">
			<h2>
				Want to go back?
			</h2>
		</router-link>
	</div>
</template>

<script>
	export default {}
</script>

<style scoped>
	.home {
		padding: 30px;
	}

	.home h2 {
		background: #42b983;
		padding: 20px;
		border-radius: 10px;
		margin: 30px auto;
		max-width: 600px;
		cursor: pointer;
		font-weight: bold;
		color: white;
		text-decoration: none;
		padding: 10px;
		border-radius: 5px;
	}
	.home h2:hover {
		color: #444;
	}
	.home a {
		text-decoration: none;
	}
</style>
