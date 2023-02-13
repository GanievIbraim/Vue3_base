<template>

  <button  @click="hide">PRESS ME</button>

  <div id='cmd_head'>
  <p>Console</p>
  </div>

  <div id='cmd'>
		<div id="block" v-for="elem in items">{{ elem**2 }}</div>
    <p>> Следующее задание</p>
    <ul>
      <li v-for="elem in items">{{ elem}}</li>
    </ul>
  </div>

</template>

<script>
export default {
	data() {
	  return {
		  items: [1, 2, 3, 4, 5],
	  }
  },

  methods: {
    hide(){
      this.isAuth = !(this.isAuth);
    }
  }
}

</script>
