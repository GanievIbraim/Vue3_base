<template>

  <button @click="">Press me!</button>

  <div id='cmd_head'>
  <p>Console</p>
  </div>
  
  <div id='cmd'>
    <p>> Task 63. Введение. Работа с компонентами в Vue.</p>
    <Employee
      v-for="user in users"
      :name="user.name"
      :salary="user.salary"
      :id="user.id"
      :age="user.age"
      :key="user.id"
	  />
  </div>

</template>

<script>
import Employee from './components/Employee.vue'

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
  components: {
		Employee
	}
}

</script>

<style>
  #cmd p, li, span{
    font-family: Consolas;
    font-size: 1.2em;
    color: rgba(0, 199, 76);
  }
</style>
