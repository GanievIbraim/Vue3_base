<template>

  <button @click="block">Block</button>

  <div id='cmd_head'>
  <p>Console</p>
  </div>
  
  <div id='cmd'>
    <p>> Task 1. Введите текст.</p>
    <input v-on:keypress.enter="submit" v-model="txt">
    <p>{{ task1 }}</p>

    <p>> Task 2. Нажмите на ссылку.</p>
    <a @click.ctrl="link">Press me + CTRL</a>
    <p>> {{ task2 }}</p>

    <p>> Task 3. Нажмите на ссылку.</p>
    <a @click.left="link1" @click.right="link2" @click.middle="link3">Press me</a>
    <p>> {{ task3 }}</p>
  </div>

</template>

<script>
let date = new Date();

export default {
	data() {
    return {
      task1: "",
      txt: "",

      task2: "",
      task3: "",
    }
  },

  methods: {
    submit: function() {
      this.task1 = this.txt;
    },
    link: function() {
      this.task2 = "Вы нажали на ссылку с зажатым CTRL.";
    },
    link1: function() {
      this.task3 = "left";
    },
    link2: function() {
      this.task3 = "right";
    },
    link3: function() {
      this.task3 = "middle";
    },
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
