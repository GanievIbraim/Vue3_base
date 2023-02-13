<template>

  <button  @click="push_num(nums)">PUSH</button>
  <button  @click="del_last(nums)">DELETE LAST</button>
  <button  @click="del_first(nums)">DELETE FIRST</button>
  <button  @click="del_last2(nums)">DELETE LAST LAST</button>
  <button  @click="sort_num(nums)">SORT</button>
  <button  @click="sort_num_inv(nums)">SORT INV</button>

  <div id='cmd_head'>
  <p>Console</p>
  </div>

  <div id='cmd'>
    <p>> Задание 1. Вывести только положительные числа.</p>
    <ul>
      <li v-for="num in nums">{{ num }}</li>
    </ul>  
  </div>

</template>

<script>
export default {
	data() {
	  return {
		  nums: [1, 2, 3],
	  }
  },

  methods: {
    push_num(arr){
      arr.push(arr.length + 1);
    },
    del_first(arr){
      arr.splice(0,1);
    },
    del_last(arr){
      arr.splice(arr.length - 1);
    },
    del_last2(arr){
      arr.splice(arr.length - 2, 1);
    },
    compare(a, b) {
      if (a > b) return 1;
      if (a == b) return 0;
      if (a < b) return -1;
    },
    sort_num(arr){
      arr.sort(this.compare);
    },
    compare_inv(a, b) {
      if (a < b) return 1;
      if (a == b) return 0;
      if (a > b) return -1;
    },
    sort_num_inv(arr){
      arr.sort(this.compare_inv);
    },
  }
}

</script>
