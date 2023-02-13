<template>

  <button  @click="hide">PRESS ME</button>

  <div id='cmd_head'>
  <p>Console</p>
  </div>

  <div id='cmd'>
    <template v-if="isAuth">
		  <p>> Абзац номер 1</p>
		  <p>> Paragraph number 2</p>
		  <p>> la la</p>
    </template>
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
