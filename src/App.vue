<template>

  <button @click="addItem">Press me!</button>

  <div id='cmd_head'>
  <p>Console</p>
  </div>
  
  <div id='cmd'>
    <p>> Task 1. Введите текст.</p>
    <input v-model="newItem">
    <ul>
      <li v-for="(item, index) in arr" :key="index">
			  {{ item }}
		  </li>
    </ul>
  </div>

</template>

<script>
let date = new Date();

export default {
	data() {
    return {
      newItem: '',
      arr: ['lala', 'haha', 'hola', 'Mavile'],
    }
  },

  methods: {
    addItem: function() {
		  this.arr.unshift(this.newItem);
	  }
  }
}

</script>

<style>
  #cmd p, li, span{
    font-family: Consolas;
    font-size: 1.2em;
    color: rgba(0, 199, 76, 0.709);
  }
  textarea{
    color: black;
  }
</style>
