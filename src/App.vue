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
        <template v-if="!user.isEdit">
          <th> {{ user.id }} </th>
          <th> {{ user.name }} </th>
          <th> {{ user.salary }} </th>
          <th> {{ user.age }} </th>
          <th @click="removeItem(user.id)"> del </th>
          <th @click="editItem(user)"> edit </th>
        </template>

        <template v-else>
          <p>> Edit forms</p>
          <span>Name: </span><input v-model="user.name"><br>
          <span>Salary: </span><input v-model="user.salary"><br>
          <span>Age: </span><input v-model="user.age"><br>
          <button @click="save(user)" id="save_but">
					  save
				  </button>
        </template>
        
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
          isEdit: false,
        },
        {
          id: 2,
          name: 'name2',
          salary: 200,
          age: 40,
          isEdit: false,
        },
        {
          id: 3,
          name: 'name3',
          salary: 300,
          age: 50,
          isEdit: false,
        },
		  ],
    }
  },

  methods: {
    removeItem: function(id) {
		  this.users = this.users.filter((user) => {
			  return user.id !== id;
		  })
	  },
    editItem: function(user) {
		  user.isEdit = true;
	  },
    save: function(user){
      user.isEdit = false;
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
    padding: 0 10px;
  }
  #save_but, input{
    font-size: 1.2em;
    color: rgba(0, 199, 76);
    background: none;
    margin-bottom: 5px;
    border: 1px solid rgba(0, 199, 76);
  }
  input{
    border: none;
    font-size: 1em;
    margin: 5px 0; 
  }
</style>
