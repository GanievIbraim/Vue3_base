<template>
    <button @click="$emit('func', 'Ibraim', '3000$')">Button number 1</button>

</template>

<script>
    export default {
        emits: ['func'],
        data() {
            return {

            }
        },
        methods: {}
    }
</script>