<template>
	<p>> {{ name }} {{ surn }} {{ age }}</p>
</template>

<script>
	export default {
        props: ['name', 'surn', 'age'],
		data() {
			return {

			}
		}
	}
</script>