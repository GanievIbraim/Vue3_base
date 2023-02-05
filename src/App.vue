<template>

  <div id='cmd_head'>
  <p>Console</p>
  </div>

  <div id='cmd'>
    <p>> Hello!</p>
  </div>
  <button @mouseover="show">OK</button>
</template>

<script>
let now = new Date();

export default {
	data() {
  },
  methods: {
	  show: function() {
		  alert(now);
	  }
  }
}
</script>
