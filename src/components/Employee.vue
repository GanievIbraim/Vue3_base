<template>
    <template v-if="!isEdit">
        <p>> {{ name }} </p>
        <p>> {{ surn }} </p>
        <button id="but" @click="edit">
            edit
        </button> <br>
    </template>
    <template v-else>
        <input v-model="newName">
        <input v-model="newSurn">
        <button id="but" @click="save">
            save
        </button> <br>
    </template>
</template>

<script>
    export default {
        props: {
            id: Number,
            name: String,
            surn: String,
        },
        emits: ['change'],
        data() {
            return {
                isEdit: false,
                newName: this.name,
                newSurn: this.surn,
            }
        },
        methods: {
            edit() {
                this.isEdit = true;
            },
            save() {
                this.isEdit = false;
                this.$emit('change', this.id, this.newName, this.newSurn);
            }
        }
    }
</script>