<template>

  <button  @click="hide">PRESS ME</button>

  <div id='cmd_head'>
  <p>Console</p>
  </div>

  <div id='cmd'>
    <ul>
      <li v-for="(elem, key) in arr"> Ключу {{ key }} соответсвует значение {{ elem }}</li>
    </ul>
  </div>

</template>

<script>
export default {
	data() {
	  return {
		  arr: ['x', 'y', 'z'],
	  }
  },

  methods: {
    hide(){
      this.isAuth = !(this.isAuth);
    }
  }
}

</script>
