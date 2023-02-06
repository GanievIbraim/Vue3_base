<template>

  <div id='cmd_head'>
  <p>Console</p>
  </div>

  <div id='cmd'>
    <p>> Hello!</p>
    <p>> Цена продукта: {{ cost }}</p>
    <p>> Количество: {{ amount }}</p>
    <p>> Сумма: {{ price }}</p>
    <p>> Нажмите на кнопку, чтобы добавить к количеству</p>
  </div>
  <button @click="show(1)">1</button>
  <button @click="show(2)">2</button>
  <button @click="show(3)">3</button>
</template>

<script>

export default {
	data() {
    return {
      cost: 43,
      amount: 5,
	  }
  },

  computed: {
    price: function() {
		  return this.cost * this.amount;
	  }
  },

  methods: {
    show: function(param) {
		  this.amount += param;
	  }
  }
}

</script>
