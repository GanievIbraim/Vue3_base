<template>

  <button @click="press">Task 1</button>

  <div id='cmd_head'>
  <p>Console</p>
  </div>
  
  <div id='cmd'>
    <p>> Task 1</p>
    <input type="checkbox" v-model="checked">
	  <p v-if="checked">> Вы видите этот абзац.</p>
  </div>

</template>

<script>
export default {
	data() {
    return {
      checked: false,
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
  #cmd p, li, textarea{
    font-family: Consolas;
    font-size: 1.2em;
    color: rgba(0, 199, 76, 0.709);
  }
  textarea{
    color: black;
  }
</style>
