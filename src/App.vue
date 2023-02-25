<template>

  <div id='cmd_head'>
    <p>Console</p>
  </div>

  <div id='cmd'>
    <p>> Task 67. Реактивное удаление компонентов в Vue.</p>
    <Employee v-for="user in users" :id="user.id" :name="user.name" :surn="user.surn" @remove="remove" :key="user.id" />
  </div>

</template>

<script>
  import Employee from './components/Employee.vue'

  export default {
    data() {
      return {
        users: [{
            id: 1,
            name: 'name1',
            surn: 'surn1'
          },
          {
            id: 2,
            name: 'name2',
            surn: 'surn2'
          },
          {
            id: 3,
            name: 'name3',
            surn: 'surn3'
          },
        ],
      }
    },
    components: {
      Employee
    },
    methods: {
      remove(id) {
        this.users = this.users.filter((user) => {
          return user.id !== id;
        })
      }
    }
  }
</script>

<style>
  #cmd p,
  li,
  span {
    font-family: Consolas;
    font-size: 1.2em;
    color: rgba(0, 199, 76);
  }
</style>