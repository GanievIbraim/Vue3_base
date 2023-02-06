<template>

  <div id='cmd_head'>
  <p>Console</p>
  </div>

  <div id='cmd'>
    <p v-if="!hidden">> Hello :)</p>
  </div>

  <button  @click="show">1</button>

</template>

<script>

export default {
	data() {
    return {
      hidden: true,
	  }
  },

  methods: {
    show: function() {
    }
  }
}

</script>
