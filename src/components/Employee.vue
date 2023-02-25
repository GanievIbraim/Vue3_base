<template>
    <button @click="x">Button number 1</button>

</template>

<script>
    export default {
        emits: ['func'],
        data() {
            return {

            }
        },
        methods: {
            x() {
                this.$emit('func', 'Ibraim', '2000$');
            }
        }
    }
</script>