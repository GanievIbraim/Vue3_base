<template>

  <button @click="">Press me!</button>

  <div id='cmd_head'>
  <p>Console</p>
  </div>
  
  <div id='cmd'>
    <p>> Task 60. Введение. Работа с компонентами в Vue.</p>
    <Employee :name_person="name" :salary="salary" :age="age" />
  </div>

</template>

<script>
import Employee from './components/Employee.vue'

export default {
  data() {
    return {
      name: 'John',
      salary: '2000',
      age: 25,
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
