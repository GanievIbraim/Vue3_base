<template>

  <button @click="">Press me!</button>

  <div id='cmd_head'>
  <p>Console</p>
  </div>
  
  <div id='cmd'>
    <p>> Нажмите на элемент списка для удаления</p>
    <table>
      <tr>
        <th>id</th>
        <th>name</th>
        <th>salary</th>
        <th>age</th>
      </tr>
      <tr v-for="user in users" :key="user.id">
        <th> {{ user.id }} </th>
        <th> {{ user.name }} </th>
        <th> {{ user.salary }} </th>
        <th> {{ user.age }} </th>
        <th @click="removeItem(user.id)"> del </th>
      </tr>
    </table>
  </div>

</template>

<script>
let date = new Date();

export default {
	data() {
    return {
      users: [
        {
          id: 1,
          name: 'name1',
          salary: 100,
          age: 30,
        },
        {
          id: 2,
          name: 'name2',
          salary: 200,
          age: 40,
        },
        {
          id: 3,
          name: 'name3',
          salary: 300,
          age: 50,
        },
		  ],
    }
  },

  methods: {
    removeItem: function(id) {
		  this.users = this.users.filter((user) => {
			  return user.id !== id;
		  })
	  }
  }
}

</script>

<style>
  #cmd p, li, span{
    font-family: Consolas;
    font-size: 1.2em;
    color: rgba(0, 199, 76);
  }
  textarea{
    color: black;
  }
  table{
    border-collapse: collapse; 
    
  }
  th{
    border: 1px solid rgba(0, 199, 76);
    color: rgba(0, 199, 76);
    width: 60px;
  }
</style>
