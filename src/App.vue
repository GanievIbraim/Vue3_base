<template>

  <button  @click="hide">PRESS ME</button>

  <div id='cmd_head'>
  <p>Console</p>
  </div>

  <div id='cmd'>
		<p v-show="isAuth">> Абзац номер 1</p>
  </div>

</template>

<script>
export default {
	data() {
    return {
      isAuth: true,
	  }
  },

  methods: {
    hide(){
      this.isAuth = !(this.isAuth);
    }
  }
}

</script>
