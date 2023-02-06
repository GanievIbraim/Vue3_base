<template>

  <div id='cmd_head'>
  <p>Console</p>
  </div>

  <div id='cmd'>
    <p>> Hello!</p>
    <p>> Для получения квдарта числа нажмите на кнопку!</p>
  </div>
  <button @click="show('0')">??</button>
  <button @click="show('2')">2</button>
  <button @click="show('3')">3</button>
</template>

<script>

export default {
	data() {
    return {
	  }
  },

  methods: {
	  show: function(param) {
      let num = Number(param);
      if (num == 0){
        num = Math.round(Math.random(100) * 100);
        alert("Квадрат числа " + num + " = " + (num * num));
        return;
      }
      alert("Квадрат числа " + num + " = " + (num * num));
	  },
  }
}

</script>
