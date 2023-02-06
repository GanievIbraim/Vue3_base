<template>

  <button  @click="one">PRESS ME</button>

  <div id='cmd_head'>
  <p>Console</p>
  </div>

  <div id='cmd'>
    <p v-if="day === 'Понедельник'">> Понедельник</p>
    <p v-if="day === 'Вторник'">> Вторник</p>
    <p v-if="day === 'Среда'">> Среда</p>
    <p v-if="day === 'Четверг'">> Четверг</p>
    <p v-if="day === 'Пятница'">> Пятница</p>
    <p v-if="day === 'Суббота'">> Суббота</p>
    <p v-if="day === 'Воскресенье'">> Воскресенье</p>
  </div>

</template>

<script>
var days =["Воскресенье", "Понедельник", "Вторник", "Среда", "Четверг", "Пятница", "Суббота"];
var now = new Date();

export default {
	data() {
    return {
      day: days[now.getDay()],
	  }
  },

  methods: {
    one: function() {
    },
  }
}

</script>
