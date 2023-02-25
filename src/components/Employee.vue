<template>
    <template v-if="!isEdit">
        <p>Пользователь номер {{ id }}</p>
        <p>Имя: {{ name }}</p>
        <p>Фамилия: {{ surn }}</p>
        <button @click="edit">edit</button><br>
    </template>
    <template v-else>
        <input v-model="newName">
        <input v-model="newSurn">
        <button @click="save">
            save
        </button>
    </template>
</template>

<script>
    export default {
        emits: ['change'],
        props: {
            id: Number,
            name: String,
            surn: String,
        },
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