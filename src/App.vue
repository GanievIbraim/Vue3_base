<template>

  <button  @click="one">PRESS ME</button>

  <div id='cmd_head'>
  <p>Console</p>
  </div>

  <div id='cmd'>
    <p v-if="age <= 18">> Подросток</p>
	  <p v-else-if=" 19 < age < 25">> Молодой человек</p>
	  <p v-else-if="age >= 26">> Мужчина</p>
	  <p v-else>error</p>
  </div>

</template>

<script>
export default {
	data() {
    return {
      age: 25,
	  }
  },

  methods: {
  }
}

</script>
