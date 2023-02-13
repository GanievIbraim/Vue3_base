<template>

  <button  @click="hide">PRESS ME</button>

  <div id='cmd_head'>
  <p>Console</p>
  </div>

  <div id='cmd'>
    <p>> Задание 1</p>
    <p v-for="num in 30">Абзац номер {{ num }}</p>    
  </div>

</template>

<script>
export default {
	data() {
	  return {
		  
	  }
  },

  methods: {
    hide(){
      this.isAuth = !(this.isAuth);
    }
  }
}

</script>
