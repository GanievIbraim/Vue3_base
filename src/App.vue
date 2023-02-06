<template>

  <button  @click="one">PRESS ME</button>
  <p v-if="isAdmin" style="color: rgb(83, 199, 91);">YES :)</p>
  <p v-else style="color: rgb(238, 87, 87);"> NO :(</p>

  <div id='cmd_head' v-if="false">
  <p>Console</p>
  </div>

  <div id='cmd' v-if="false">
    <p >> Hello :)</p>
  </div>

</template>

<script>

export default {
	data() {
    return {
      isAdmin: true,
	  }
  },

  methods: {
    one: function() {
      this.isAdmin = !this.isAdmin;
    },
  }
}

</script>
