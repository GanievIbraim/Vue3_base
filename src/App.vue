<template>

  <button @click="press">Task 2</button>

  <div id='cmd_head'>
  <p>Console</p>
  </div>
  
  <div id='cmd'>
    <p>> Task 1</p>
    <textarea v-model="text"></textarea>
	  <p>{{ text }}</p>

    <p>> Task 2</p>
    <textarea v-model="txt"></textarea>
    <ul v-for="elem in arr">
      <li>{{ elem }}</li>
    </ul>
  </div>

</template>

<script>
export default {
	data() {
    return {
      text: 0,
      txt: 0,
      arr: [],
    }
  },

  methods: {
    press: function() {
      this.arr = this.txt.split(" ");
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
