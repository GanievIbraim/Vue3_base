<template>

  <button  @click="hide">PRESS ME</button>

  <div id='cmd_head'>
  <p>Console</p>
  </div>

  <div id='cmd'>
    <p>> Задание 1. Вывести только положительные числа.</p>
    <ul>
      <li v-for="product in products" :key="product.id">{{ product.name }}</li>
    </ul>  
  </div>

</template>

<script>
export default {
	data() {
	  return {
		  products: [
        {
          id: 1,
          name: 'Product_1',
        },
        {
          id: 2,
          name: 'Product_2',
        },
        {
          id: 3,
          name: 'Product_3',
        },
		  ],
	  }
  },

  methods: {
    hide(){
      this.isAuth = !(this.isAuth);
    }
  }
}

</script>
