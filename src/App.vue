<template>

  <button>Press me</button>

  <div id='cmd_head'>
  <p>Console</p>
  </div>
  
  <div id='cmd'>
    <p>> Введите текст</p>
    <input v-model="task2">
    <p>> {{task2}}</p>

    <p>> Введите число</p>
    <input v-model="task3">
    <p>> {{ task3 * task3}}</p>
  </div>

</template>

<script>
export default {
	data() {
	return {
    task3: 'hello',
    task2: 'qwert',
	}
},

  methods: {
  }
}

</script>

<style>
  #cmd p{
    font-family: Consolas;
    font-size: 1.2em;
    color: rgba(0, 199, 76, 0.709);
    text-transform: uppercase;
  }
</style>
