<template>

  <button @click="hide">Hide</button>
  <button @click="show">Show</button>
  <button @click="toggle">Toggle</button>

  <div id='cmd_head'>
  <p>Console</p>
  </div>
  
  <div id='cmd'>
    <p :class="obj">> Задание 39. Теперь этот абзац тоже виден.</p>
    <p class="done">> Задание 39. Этот абзац видно, a первый нет.</p> 
  </div>

</template>

<script>
export default {
	data() {
	return {
		obj: {
			hidden: true,
      done: true,
		},
	}
},

  methods: {
    hide: function() {
		  this.obj.hidden = true;
	  },
    show: function() {
      this.obj.hidden = false;
    },
    toggle: function() {
      this.obj.hidden = !this.obj.hidden;
    }
  }
}

</script>

<style>
  .done{
    font-family: Consolas;
    font-size: 1.5em;
    color: rgb(4, 194, 118);
  }
  p.hidden {
	  display: none;
}
</style>
