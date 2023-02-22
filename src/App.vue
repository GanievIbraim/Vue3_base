<template>

  <button @click="press">Task 1</button>

  <div id='cmd_head'>
  <p>Console</p>
  </div>
  
  <div id='cmd'>
    <p>> Task 1. В каком городе вы живете.</p>
    <select v-model="selected">
		  <option>Симферополь</option>
		  <option>Алушта</option>
		  <option>Судак</option>
      <option>Феодосия</option>
      <option>Джанкой</option>
	  </select>
    
    <p>> {{ selected }}</p>
    
  </div>

</template>

<script>
export default {
	data() {
    return {
      selected: "",
    }
  },

  methods: {
    press: function() {
      this.checked = !this.checked;
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
