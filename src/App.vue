<template>

  <div id='cmd_head'>
  <p>Console</p>
  </div>

  <div id='cmd'>
    <p>> Hello!</p>
  </div>
  <button @click="show">OK</button>
</template>

<script>
let now = new Date();

export default {
	data() {
    return {
		num1: 23,
		num2: 100,
	  }
  },

  methods: {
	  show: function() {
		  alert(this.num1 + this.num2);
	  }
  }
}
</script>
