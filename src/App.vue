<template>

  <button @click="press">Task 1</button>

  <div id='cmd_head'>
  <p>Console</p>
  </div>
  
  <div id='cmd'>
    <p>> Task 1</p>
    <input type="checkbox" v-model="arr" value="Python"> <span>Python</span><br>
	  <input type="checkbox" v-model="arr" value="Java"> <span>Java</span><br>
	  <input type="checkbox" v-model="arr" value="JS"> <span>JS</span><br>
    <input type="checkbox" v-model="arr" value="C++"> <span>C++</span><br>
    <input type="checkbox" v-model="arr" value="C"> <span>C</span><br>
    <input type="checkbox" v-model="arr" value="GO"> <span>GO</span><br>
    <input type="checkbox" v-model="arr" value="Ruby"> <span>Ruby</span><br>
    <p>> Количество:  {{ arr.length }}</p>
    <p>> Cписок языков:</p>
    <ul v-for="elem in arr">
      <li>{{ elem }}</li>
    </ul>
  </div>

</template>

<script>
export default {
	data() {
    return {
      arr: [],
    }
  },

  methods: {
    press: function() {
      this.checked = !this.checked;
    }
  }
}

</script>

<style>
  #cmd p, li, span{
    font-family: Consolas;
    font-size: 1.2em;
    color: rgba(0, 199, 76, 0.709);
  }
  textarea{
    color: black;
  }
</style>
