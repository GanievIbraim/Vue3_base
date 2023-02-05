<template>
  <div id='cmd_head'>
  <p>Console</p>
  </div>

  <div id='cmd'>
    <p>> RESULT: {{ obj.x + obj.y + obj.z + obj.w}}</p>
  </div>
</template>

<script>
export default {
	data() {
	  return {
		  obj: {x: 444, y: 333, z: 222, w: 1},
	  }
  } 
}

</script>
