<template>
    <p> Работник номер {{ id }}</p>
	<p> Name: {{ name }} </p>
    <p> Salary: {{ salary }}$ </p>
    <p>  Age: {{ age }}</p> <br>
</template>

<script>
	export default {
        props: {
            name: String,
            salary: Number,
            id: Number,
            age: Number,
        },
		data() {
			return {

			}
		}
	}
</script>