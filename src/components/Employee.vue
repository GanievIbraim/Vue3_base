<template>
	<p> Name: {{ name_person }} </p>
    <p> Salary: {{ salary }}$ </p>
    <p>  Age: {{ age }}</p>
</template>

<script>
	export default {
        props: ['name_person', 'salary', 'age'],
		data() {
			return {

			}
		}
	}
</script>