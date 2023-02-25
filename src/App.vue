<template>

  <div id='cmd_head'>
    <p>Console</p>
  </div>

  <div id='cmd'>
    <p>> Task 65. Введение. Работа с компонентами в Vue.</p>
    <Employee @func="func" />
  </div>

</template>

<script>
  import Employee from './components/Employee.vue'

  export default {
    data() {
      return {

      }
    },
    components: {
      Employee
    },
    methods: {
      func(name, salary) {
		console.log(name, salary);
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