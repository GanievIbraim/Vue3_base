<template>
    <button @click="x">Button number 1</button>
    <button @click="y">Button number 2</button>
</template>

<script>
    export default {
        emits: ['first', 'second'],
        data() {
            return {

            }
        },
        methods: {
            x() {
                this.$emit('first');
            },
            y() {
                this.$emit('second');
            }
        }
    }
</script>