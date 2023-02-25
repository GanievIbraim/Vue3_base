<template>

  <button @click="">Press me!</button>

  <div id='cmd_head'>
  <p>Console</p>
  </div>
  
  <div id='cmd'>
    <p>> Нажмите на элемент списка для удаления</p>
    <ul>
      <li v-for="(item, index) in arr" :key="index" @click="removeItem(index)">
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
      arr: ['lala', 'haha', 'hola', 'Mavile'],
    }
  },

  methods: {
    removeItem: function(index) {
		  this.arr.splice(index, 1);
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
