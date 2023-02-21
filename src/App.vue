<template>

  <button>Press me</button>

  <div id='cmd_head'>
  <p>Console</p>
  </div>
  
  <div id='cmd'>
    <p :class="{active: true, valid: false}">> Задание 40. Теперь этот абзац тоже виден.</p>
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
  .active{
    font-family: Consolas;
    font-size: 1.5em;
    color: rgb(4, 194, 118);
  }
  .valid{
	  text-decoration: underline;
}
</style>
