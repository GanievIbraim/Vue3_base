<template>

  <div id='cmd_head'>
  <p>Console</p>
  </div>

  <div id='cmd'>
    <p>> Hello!</p>
  </div>
  {{ show() }}
  <!-- <button @click="show">OK</button> -->
</template>

<script>
let arr = prompt('Введите чсило от 1 до 7!')
let week =[
      'Понедельник',
      'Вторник',
      'Среда',
      'Четверг',
      'Пятница',
      'Суббота',
      'Воскресенье'
];

export default {
	data() {
    return {
      days: week,
      param: Number(arr),
	  }
  },

  methods: {
	  show: function() {
		  let day = this.cape(this.param);
      let now = new Date();

      alert("Ваш день недели: " + day);
      alert("Cегодняшний день недели: " + week[now.getDay() - 1]);
	  },

    cape: function(num) {
      if (num > 7 || num < 1){
        return 'Число не входит в диапазон от 1 до 7';
      }
      return this.days[num-1];    
    }
  }
}

</script>
