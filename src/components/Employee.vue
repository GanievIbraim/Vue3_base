<template>
	{{ name }}
	{{ surn }}
    <button @click="$emit('remove', id)">
		remove
	</button>
    <br>
</template>

<script>
    export default {
        props: {
            id: Number,
            name: String,
            surn: String,
        },
        emits: ['remove'],
        data() {
            return {

            }
        },
        methods: {}
    }
</script>