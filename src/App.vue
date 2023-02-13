<template>

  <button  @click="hide">PRESS ME</button>

  <div id='cmd_head'>
  <p>Console</p>
  </div>

  <div id='cmd'>
    <div v-for="elem in items">
	    <p>> {{ elem }}</p>
	    <p class="divider"></p>
    </div>

    <ul v-for="elem in items">
      <li>{{ elem }}</li>
      <li class="divider"></li>
    </ul>
  </div>

</template>

<script>
export default {
	data() {
	  return {
		  items: [1, 2, 3],
	  }
  },

  methods: {
    hide(){
      this.isAuth = !(this.isAuth);
    }
  }
}

</script>
