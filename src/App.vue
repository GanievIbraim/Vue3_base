<template>

  <button  @click="hide">PRESS ME</button>

  <div id='cmd_head'>
  <p>Console</p>
  </div>

  <div id='cmd'>
    <p>> Задание 1</p>
    <ul>
      <li v-for="elem in hrefs"><a :href="elem.href">{{elem.text}}</a></li>
    </ul>
    <p>> Задание 2</p>
    <table>
      <td>Название </td> 
      <td>Цена </td>  
      <td>Количество </td>
      <tr v-for="product in products">
        <td>{{ product.name }}</td>
        <td>{{ product.price }}</td>
        <td>{{ product.quantity }}</td>
      </tr>
    </table>
  </div>

</template>

<script>
export default {
	data() {
	  return {
		  hrefs: [
        {href: '1.html', text: 'text1'},
        {href: '2.html', text: 'text2'},
        {href: '3.html', text: 'text3'},
		  ],
      products: [
        {
          name: 'Product_2',
          price: 100,
          quantity: 5
        },
        {
          name: 'Product_2',
          price: 200,
          quantity: 4
        },
        {
          name: 'Product_3',
          price: 300,
          quantity: 3
        },
		  ]
	  }
  },

  methods: {
    hide(){
      this.isAuth = !(this.isAuth);
    }
  }
}

</script>
