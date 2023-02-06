<template>

  <div id='cmd_head'>
  <p>Console</p>
  </div>

  <div id='cmd'>
    <p>> Hello!</p>
    <p>> Для получения квдарта числа нажмите на кнопку!</p>
    <p>> {{ text }}</p>
  </div>
  <button @click="show('1')">1</button>
  <button @click="show('2')">2</button>
  <button @click="show('3')">3</button>
</template>

<script>

export default {
	data() {
    return {
      text: "",
	  }
  },

  methods: {
	  show: function(param) {
      this.text = ' Вы нажали на кнопку №' + param;
	  },
  }
}

</script>
