<template>

  <button @click="press">Task 1</button>

  <div id='cmd_head'>
  <p>Console</p>
  </div>
  
  <div id='cmd'>
    <p>> Task 1. Выберете родной язык.</p>
    <input name="radio" type="radio" v-model="choice" value="rus"> 
    <span> Русский</span><br>

	  <input name="radio" type="radio" v-model="choice" value="tat"> 
    <span> Крымскотатарский</span><br>

	  <input name="radio" type="radio" v-model="choice" value="eng">
    <span> Английский</span><br>
    <p v-if="choice == 'rus'">> Русский язык</p>
    <p v-if="choice == 'tat'">> Къырымтатар тили</p>
    <p v-if="choice == 'eng'">> English language</p>
    
  </div>

</template>

<script>
export default {
	data() {
    return {
      choice: "",
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
