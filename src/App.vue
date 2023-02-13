<template>

  <button  @click="hide">PRESS ME</button>

  <div id='cmd_head'>
  <p>Console</p>
  </div>

  <div id='cmd'>
    <p>> Задание 1. Вывести только положительные числа.</p>
    <template v-for="elem in items">
			<p v-if="elem > 0">
				> {{ elem }}
      </p>
		</template>  
  </div>

</template>

<script>
export default {
	data() {
	  return {
		  items: [1, -2, 3, -4, 5],
	  }
  },

  methods: {
    hide(){
      this.isAuth = !(this.isAuth);
    }
  }
}

</script>
