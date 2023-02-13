<template>

  <button  @click="hide">PRESS ME</button>

  <div id='cmd_head'>
  <p>Console</p>
  </div>

  <div id='cmd'>
    <ul>
      <li v-for="(elem, key, index) in obj">> {{ key }} - {{ elem }} - {{ index + 1 }} </li>
    </ul>
  </div>

</template>

<script>
export default {
	data() {
	  return {
		  obj: {
            user1: '100$',
            user2: '200$',
            user3: '300$',
          },
	  }
  },

  methods: {
    hide(){
      this.isAuth = !(this.isAuth);
    }
  }
}

</script>
