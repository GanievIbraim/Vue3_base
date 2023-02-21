<template>

  <button>PRESS ME</button>

  <div id='cmd_head'>
  <p>Console</p>
  </div>

  <div id='cmd'>
    <p :class="obj">> Задание 38. Объект с CSS классами в Vue.</p> 
  </div>

</template>

<script>
export default {
	data() {
	  return {
      obj: {
			  done: true,
			  selected:  false,
		  },
	  }
  },

  methods: {
  }
}

</script>

<style>
  .done{
    font-family: Consolas;
    font-size: 1.5em;
    color: rebeccapurple;
  }
  .selected{
    color: #54916c;
  }
</style>
