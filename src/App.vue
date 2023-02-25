<template>

  <div id='cmd_head'>
    <p>Console</p>
  </div>

  <div id='cmd'>
    <p>> Task 69. Реактивное редактирование данных компонента.</p>
    <Employee v-for="user in users" :id="user.id" :name="user.name" :surn="user.surn" :key="user.id" @change="change" />
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
      change(id, name, surn) {
        this.users = this.users.map((user) => {
          if (user.id === id) {
            user.name = name;
            user.surn = surn;
          }
          return user;
        });
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

  button,
  input {
    margin-left: 20px;
    font-family: Consolas;
    font-size: 1.2em;
    background: none;
    color: #00c74c;
    border: 1px solid #00c74c;
  }
</style>