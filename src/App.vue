<template>

  <button @click="">Press me!</button>

  <div id='cmd_head'>
  <p>Console</p>
  </div>
  
  <div id='cmd'>
    <p>> Task 58. Введение. Работа с компонентами в Vue.</p>
    <User />
  </div>

</template>

<script>
import User from './components/Employee.vue'

export default {
  components: {
		User
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
