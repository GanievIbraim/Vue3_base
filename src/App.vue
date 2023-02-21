<template>

  <button>PRESS ME</button>

  <div id='cmd_head'>
  <p>Console</p>
  </div>

  <div id='cmd'>
    <p :class="cssClasses">> Задание 37. Атрибут class в фреймворке Vue.</p> 
  </div>

</template>

<script>
export default {
	data() {
	  return {
      cssClasses: "txt",
	  }
  },

  methods: {
  }
}

</script>

<style>
  .txt{
    font-family: Consolas;
    font-size: 1.5em;
    color: #54916c;
}
</style>
