<template>
	<div v-if="job">
		<h1>{{ job.title }}</h1>
		<p>The job id is: {{ id }}</p>
		<p>{{ job.description }}</p>
	</div>
	<div v-else>
		<p>Loading job details...</p>
	</div>
</template>

<script>
	export default {
		//ID von den rout params
		props: ["id"],
		// data() {
		// 	return {
		// 		id: this.$route.params.id,
		// 	}
		// },
		data() {
			return {
				job: null,
			}
		},
		mounted() {
			fetch("http://localhost:3000/jobs/" + this.id)
				.then((res) => res.json())
				.then((data) => (this.job = data))
				.catch((error) => console.log(error.message()))
		},
	}
</script>

<style></style>
