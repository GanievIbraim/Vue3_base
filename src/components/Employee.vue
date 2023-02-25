<template>
	<p> Name: {{ name_person }} </p>
    <p> Salary: {{ salary }}$ </p>
    <p>  Age: {{ age }}</p>
</template>

<script>
	export default {
        props: {
            name_person: String,
            salary: String,
            age: Number,
        },
		data() {
			return {

			}
		}
	}
</script>