<template>

  <button @click="block">Block</button>

  <div id='cmd_head'>
  <p>Console</p>
  </div>
  
  <div id='cmd'>
    <p>> Task 1. Выберите день недели.</p>
    <input v-bind:disabled="isDisabled">
    <br>
    <input type="checkbox" v-model="isDisabled"> <span>Заблокировать input</span>

  </div>

</template>

<script>
let date = new Date();

export default {
	data() {
    return {
      isDisabled: true,
    }
  },

  methods: {
    block: function() {
      this.isDisabled = !this.isDisabled;
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
