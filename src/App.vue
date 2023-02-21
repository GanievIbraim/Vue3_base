<template>

  <button>Press me</button>

  <div id='cmd_head'>
  <p>Console</p>
  </div>
  
  <div id='cmd'>
    <p :style="{color: 'rgb(4, 194, 118)', 'background-color': 'yellow'}">> Задание 42. Зеленый шрифт с желтым фоном.</p>
    <p :style="{'font-style': 'italic', 'font-weight': 'bold'}">> Задание 42. Абзац жирный и курсивный.</p>
  </div>

</template>

<script>
export default {
	data() {
	return {
	}
},

  methods: {
  }
}

</script>

<style>

</style>
