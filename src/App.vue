<template>
  <button  @click="hide" v-if="visible">HIDE</button>
  <button  @click="show" v-if="!visible">SHOW</button>

  <div id='cmd_head' v-if="visible">
  <p>Console</p>
  </div>

  <div id='cmd' v-if="visible">
    <p >> Hello :)</p>
  </div>

  
</template>

<script>

export default {
	data() {
    return {
      visible: true,
	  }
  },

  methods: {
    show: function() {
      this.visible = true;
    },
    hide: function() {
      this.visible = false;
    }
  }
}

</script>
