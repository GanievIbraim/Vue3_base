<template>

  <div id='cmd_head'>
    <p>Console</p>
  </div>

  <div id='cmd'>
    <p>> Task 70. Компонент для добавления данных в Vue.</p>
    <Employee v-for="user in users" :id="user.id" :name="user.name" :surn="user.surn" :key="user.id" @change="change" />
    <UserForm @add="add" />
  </div>

</template>

<script>
  import Employee from './components/Employee.vue'
  import UserForm from './components/UserForm.vue'

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
      Employee,
      UserForm
    },
    methods: {
      add(name, surn) {
        let id = this.users.length + 1;

        this.users.push({
          id,
          name,
          surn
        });
      },
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
  #cmd p {
    font-family: Consolas;
    font-size: 1.2em;
    color: rgba(0, 199, 76);
    margin-left: 10px;
  }

  button,
  input {
    margin-bottom: 10px;
    margin-left: 10px;
    font-family: Consolas;
    font-size: 1.2em;
    background: none;
    color: #00c74c;
    border: 1px solid #00c74c;
  }
</style>